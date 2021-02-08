   
# 1 
    compile 'com.squareup.picasso:picasso:2.5.2'

    compile 'com.squareup.retrofit2:retrofit:2.3.0'
    compile 'com.squareup.retrofit2:converter-gson:2.3.0'
    compile 'com.jakewharton.picasso:picasso2-okhttp3-downloader:1.1.0'
    
# 2 
    <uses-permission android:name="android.permission.INTERNET" />
   
# 3
Create data model to parse JSON data.
  * @SerializedName
  * Constructor
  * Getter & Setter
# 4
 Create the Retrofit Instance

    public class RetrofitApiClient {

            private static final String BASE_URL = " ***api name*** ";
            private static Retrofit retrofit = null;

            private static Gson gson = new GsonBuilder()
                    .setLenient()
                    .create();

            private RetrofitApiClient() {} // So that nobody can create an object with constructor

            public static Retrofit getClient() {
            if (retrofit == null) {
                synchronized (RetrofitApiClient.class) { //thread safe Singleton implementation
                    if (retrofit == null) {
                        retrofit = new Retrofit.Builder()
                                .baseUrl(BASE_URL)
                                .addConverterFactory(GsonConverterFactory.create(gson))
                                .build();
                    }
                }
            }
            return retrofit;
        }
    }
    
# 5
     public interface ApiClient {
             * GET
             * POST
             * QUERY DATA
     }
      
## 5.1 GET
     @GET("SUB_BASE_API")
        Call< MODEL_CLASS_NAME > getData();
## 5.2 POST
    @FormUrlEncoded
    @POST("SUB_BASE_API")
    Call<MODEL_CLASS_NAME> postData(@Field("JSON_Field_Name") String StringName,
                                        @Field("JSON_Field_Name") String StringName,
                                        @Field("JSON_Field_Name") String StringName,
                                        );
## 5.3 GET
    @GET("SUB_BASE_API")
    Call<SignInResponse> queryData(@Query("JSON_Field_Name") String StringName,
                   @Query("JSON_Field_Name") String StringName,
                   @Query("JSON_Field_Name") String StringName,
                   );
              
