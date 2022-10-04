     <b-form-input required
                  id="blog-edit-excerpt_en"
                  v-model="blogEdit.excerpt_en"  @keypress="check_lang($event,'en')"
              />
