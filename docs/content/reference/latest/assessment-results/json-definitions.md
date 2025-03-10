---
title: "OSCAL Assessment Results Model v1.0.2 JSON Format Metaschema Reference"
heading: "Assessment Results Model v1.0.2 Model JSON Metaschema Reference"
weight: 40
generateanchors: false
sidenav:
  title: JSON Metaschema Reference
toc:
  enabled: true
  headingselectors: "h1.toc1, h2.toc2, h3.toc3, h4.toc4, h5.toc5, h6.toc6"
---

The following is a reference for the JSON object definitions derived from the [metaschema](https://github.com/usnistgov/OSCAL/blob/main//src/metaschema/oscal_assessment-results_metaschema.xml) for this [model](/concepts/layer/assessment/assessment-results/).

<!-- DO NOT REMOVE. Generated text below -->
{{< rawhtml >}}
<div xmlns="http://www.w3.org/1999/xhtml" class="json-definition">
   <p><span class="usa-tag">Short name</span> oscal-ar</p>
   <p><span class="usa-tag">JSON Base URI</span> <code>http://csrc.nist.gov/ns/oscal</code></p>
   <details class="remarks" open="open">
      <summary>Remarks</summary>
      <p class="p">The OSCAL assessment results format is used to describe the information typically
         provided by an assessor following an assessment.</p>
      <p class="p">The root of the OSCAL assessment results format is <code>assessment-results</code>. </p>
   </details>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-assessment-common/activity" class="toc1 name">activity</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/activity">Switch to XML</a></div>
         <p class="formal-name">Activity</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Identifies an assessment or related process that can be performed. In the assessment
            plan, this is an intended activity which may be associated with an assessment task.
            In the assessment results, this an activity that was actually performed as part of
            an assessment.</p>
         <details>
            <summary>Constraints (4)</summary>
            
            
            <div class="constraint">
               <p><span class="usa-tag">allowed value</span> for <code class="path">prop/@name</code></p>
               <p>The value <b>may be locally defined</b>, or the following:</p>
               <ul>
                  
                  <li><strong>method</strong>: The assessment method to use. This typically appears on parts with the name "assessment".</li>
                  </ul>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">has cardinality</span> for <code class="path">prop[@name='method']</code> the cardinality of  <code>prop[@name='method']</code> is constrained: <b>1</b>; maximum <b>unbounded</b>.</p>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">prop[@name='method']/@value</code></p>
               <p>The value <b>must</b> be one of the following:</p>
               <ul>
                  
                  <li><strong>INTERVIEW</strong>: The process of holding discussions with individuals or groups of individuals within
                     an organization to once again, facilitate assessor understanding, achieve clarification,
                     or obtain evidence.</li>
                  
                  <li><strong>EXAMINE</strong>: The process of reviewing, inspecting, observing, studying, or analyzing one or more
                     assessment objects (i.e., specifications, mechanisms, or activities).</li>
                  
                  <li><strong>TEST</strong>: The process of exercising one or more assessment objects (i.e., activities or mechanisms)
                     under specified conditions to compare actual with expected behavior.</li>
                  </ul>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">is unique</span> for <code class="path">responsible-role</code>: any target value must be unique (i.e., occur only once)</p>
            </div>
            </details>
         <details open="open">
            <summary>Properties (9)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/activity/uuid" class="toc2 name">uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/activity/uuid">Switch to XML</a></div>
                     <p class="formal-name">Assessment Activity Universally Unique Identifier</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this assessment activity elsewhere in <a href="/concepts/identifier-use/#scope">this or other OSCAL instances</a>. The locally defined <em>UUID</em> of the <code>activity</code> can be used to reference the data item locally or globally (e.g., in an imported
                        OSCAL instance). This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                        of the document.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/activity/title" class="toc2 name">title</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/activity/title">Switch to XML</a></div>
                     <p class="formal-name">Included Activity Title</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> The title for this included activity.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/activity/description" class="toc2 name">description</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/activity/description">Switch to XML</a></div>
                     <p class="formal-name">Included Activity Description</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A human-readable description of this included activity.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/activity/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/activity/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/activity/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/activity/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/activity/steps" class="toc2 name">step</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/activity/step">Switch to XML</a></div>
                     <p class="formal-name">Step</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Identifies an individual step in a series of steps related to an activity, such as
                        an assessment test or examination procedure.</p>
                     <p><span class="usa-tag">group as</span> <code class="name">steps</code></p>
                     <details>
                        <summary>Constraint (1)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">is unique</span> for <code class="path">responsible-role</code>: any target value must be unique (i.e., occur only once)</p>
                        </div>
                        </details>
                     <details open="open">
                        <summary>Properties (8)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition define-flag">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/activity/steps/uuid" class="toc3 name">uuid</h3>
                                 <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/activity/step/uuid">Switch to XML</a></div>
                                 <p class="formal-name">Step Universally Unique Identifier</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this step elsewhere in <a href="/concepts/identifier-use/#scope">this or other OSCAL instances</a>. The locally defined <em>UUID</em> of the <code>step</code> (in a series of steps) can be used to reference the data item locally or globally
                                    (e.g., in an imported OSCAL instance). This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                                    of the document.</p>
                              </div>
                           </div>
                           <div class="model-entry definition define-field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/activity/steps/title" class="toc3 name">title</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/activity/step/title">Switch to XML</a></div>
                                 <p class="formal-name">Step Title</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> The title for this step.</p>
                              </div>
                           </div>
                           <div class="model-entry definition define-field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/activity/steps/description" class="toc3 name">description</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                 <p class="occurrence">[1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/activity/step/description">Switch to XML</a></div>
                                 <p class="formal-name">Step Description</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A human-readable description of this step.</p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/activity/steps/props" class="toc3 name">property</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/activity/step/prop">Switch to XML</a></div>
                                 <p class="formal-name">Property</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                                 <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>Properties permit the deployment and management of arbitrary controlled values, within
                                             OSCAL objects. A property can be included for any purpose useful to an application
                                             or implementation. Typically, properties will be used to sort, filter, select, order,
                                             and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                             an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                             lexical composition of properties may be constrained by external processes to ensure
                                             consistency.</p>
                                          <p>Property allows for associated remarks that describe why the specific property value
                                             was applied to the containing object, or the significance of the value in the context
                                             of the containing object.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/activity/steps/links" class="toc3 name">link</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/activity/step/link">Switch to XML</a></div>
                                 <p class="formal-name">Link</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                             a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                                          <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/activity/steps/reviewed-controls" class="toc3 name">reviewed-controls</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/activity/step/reviewed-controls">Switch to XML</a></div>
                                 <p class="formal-name">Reviewed Controls and Control Objectives</p>
                              </div>
                              <div class="body">
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>In the context of an assessment plan, this construct is used to identify the controls
                                             and control objectives that are to be assessed. In the context of an assessment result,
                                             this construct is used to identify the actual controls and objectives that were assessed,
                                             reflecting any changes from the plan.</p>
                                          <p>When resolving the selection of controls and control objectives, the following processing
                                             will occur:</p>
                                          <p>1. Controls will be resolved by creating a set of controls based on the control-selections
                                             by first handling the includes, and then removing any excluded controls.</p>
                                          <p>2. The set of control objectives will be resolved from the set of controls that was
                                             generated in the previous step. The set of control objectives is based on the control-objective-selection
                                             by first handling the includes, and then removing any excluded control objectives.</p>
                                       </div>
                                       <div class="remarks">
                                          <p>This can be optionally used to define the set of controls and control objectives that
                                             are assessed by this step.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-assessment-common/reviewed-controls">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/activity/steps/responsible-roles" class="toc3 name">responsible-role</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/activity/step/responsible-role">Switch to XML</a></div>
                                 <p class="formal-name">Responsible Role</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">group as</span> <code class="name">responsible-roles</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>Identifies the roles, and optionally the parties, associated with this step that is
                                             part of an assessment activity.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/responsible-role">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/activity/steps/remarks" class="toc3 name">remarks</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/activity/step/remarks">Switch to XML</a></div>
                                 <p class="formal-name">Remarks</p>
                              </div>
                              <div class="body">
                                 <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/activity/related-controls" class="toc2 name">related-controls</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/activity/related-controls">Switch to XML</a></div>
                     <p class="formal-name">Reviewed Controls and Control Objectives</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">related-controls</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>In the context of an assessment plan, this construct is used to identify the controls
                                 and control objectives that are to be assessed. In the context of an assessment result,
                                 this construct is used to identify the actual controls and objectives that were assessed,
                                 reflecting any changes from the plan.</p>
                              <p>When resolving the selection of controls and control objectives, the following processing
                                 will occur:</p>
                              <p>1. Controls will be resolved by creating a set of controls based on the control-selections
                                 by first handling the includes, and then removing any excluded controls.</p>
                              <p>2. The set of control objectives will be resolved from the set of controls that was
                                 generated in the previous step. The set of control objectives is based on the control-objective-selection
                                 by first handling the includes, and then removing any excluded control objectives.</p>
                           </div>
                           <div class="remarks">
                              <p>This can be optionally used to define the set of controls and control objectives that
                                 are assessed or remediated by this activity.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-assessment-common/reviewed-controls">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/activity/responsible-roles" class="toc2 name">responsible-role</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/activity/responsible-role">Switch to XML</a></div>
                     <p class="formal-name">Responsible Role</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">responsible-roles</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Since <code>responsible-role</code> associates multiple <code>party-uuid</code> entries with a single <code>role-id</code>, each role-id must be referenced only once.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/responsible-role">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/activity/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/activity/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-field">
      <div class="definition-header">
         <h1 id="/field/oscal-metadata/addr-line" class="toc1 name">addr-line</h1>
         <p class="type"><a href="/reference/datatypes/#string">string</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-metadata/addr-line">Switch to XML</a></div>
         <p class="formal-name">Address line</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A single line of an address.</p>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-metadata/address" class="toc1 name">address</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/address">Switch to XML</a></div>
         <p class="formal-name">Address</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A postal address for the location.</p>
         <details open="open">
            <summary>Properties (6)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/address/type" class="toc2 name">type</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/address/type">Switch to XML</a></div>
                     <p class="formal-name">Address Type</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">type</code></p>
                     <p class="definition-link"><a href="#/flag/oscal-metadata/location-type">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/address/addr-lines" class="toc2 name">addr-line</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/address/addr-line">Switch to XML</a></div>
                     <p class="formal-name">Address line</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">addr-lines</code></p>
                     <p class="definition-link"><a href="#/field/oscal-metadata/addr-line">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/address/city" class="toc2 name">city</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/address/city">Switch to XML</a></div>
                     <p class="formal-name">City</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> City, town or geographical region for the mailing address.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/address/state" class="toc2 name">state</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/address/state">Switch to XML</a></div>
                     <p class="formal-name">State</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> State, province or analogous geographical region for mailing address</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/address/postal-code" class="toc2 name">postal-code</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/address/postal-code">Switch to XML</a></div>
                     <p class="formal-name">Postal Code</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Postal or ZIP code for mailing address</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/address/country" class="toc2 name">country</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/address/country">Switch to XML</a></div>
                     <p class="formal-name">Country Code</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> The ISO 3166-1 alpha-2 country code for the mailing address.</p>
                     <details>
                        <summary>Constraint (1)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">matches</span>: a target (value) must match the regular expression '[A-Z](2)'.</p>
                        </div>
                        </details>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-assessment-common/assessment-assets" class="toc1 name">assessment-assets</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-assets">Switch to XML</a></div>
         <p class="formal-name">Assessment Assets</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Identifies the assets used to perform this assessment, such as the assessment team,
            scanning tools, and assumptions.</p>
         <details>
            <summary>Constraint (1)</summary>
            
            <div class="constraint">
               <p><span class="usa-tag">is unique</span> for <code class="path">component</code>: any target value must be unique (i.e., occur only once)</p>
            </div>
            </details>
         <details open="open">
            <summary>Properties (2)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-assets/components" class="toc2 name">component</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-assets/component">Switch to XML</a></div>
                     <p class="formal-name">Component</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">component</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">components</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Components may be products, services, application programming interface (APIs), policies,
                                 processes, plans, guidance, standards, or other tangible items that enable security
                                 and/or privacy.</p>
                              <p>The <code>type</code> indicates which of these component types is represented.</p>
                              <p>When defining a <code>service</code> component where are relationship to other components is known, one or more <code>link</code> entries with rel values of provided-by and used-by can be used to link to the specific
                                 component identifier(s) that provide and use the service respectively.</p>
                           </div>
                           <div class="remarks">
                              <p>Used to add any components for tools used during the assessment. These are represented
                                 here to avoid mixing with system components.</p>
                              <p>The technology tools used by the assessor to perform the assessment, such as vulnerability
                                 scanners. In the assessment plan these are the intended tools. In the assessment results,
                                 these are the actual tools used, including any differences from the assessment plan.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-implementation-common/system-component">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-assets/assessment-platforms" class="toc2 name">assessment-platform</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[1 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-assets/assessment-platform">Switch to XML</a></div>
                     <p class="formal-name">Assessment Platform</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Used to represent the toolset used to perform aspects of the assessment.</p>
                     <p><span class="usa-tag">group as</span> <code class="name">assessment-platforms</code></p>
                     <details open="open">
                        <summary>Properties (6)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition define-flag">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/assessment-assets/assessment-platforms/uuid" class="toc3 name">uuid</h3>
                                 <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-assets/assessment-platform/uuid">Switch to XML</a></div>
                                 <p class="formal-name">Assessment Platform Universally Unique Identifier</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this assessment platform elsewhere in this or
                                    other OSCAL instances. The locally defined <em>UUID</em> of the <code>assessment platform</code> can be used to reference the data item locally or globally (e.g., in an <a href="/concepts/identifier-use/#scope">imported OSCAL instance</a>). This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                                    of the document.</p>
                              </div>
                           </div>
                           <div class="model-entry definition define-field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/assessment-assets/assessment-platforms/title" class="toc3 name">title</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-assets/assessment-platform/title">Switch to XML</a></div>
                                 <p class="formal-name">Assessment Platform Title</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> The title or name for the assessment platform.</p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/assessment-assets/assessment-platforms/props" class="toc3 name">property</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-assets/assessment-platform/prop">Switch to XML</a></div>
                                 <p class="formal-name">Property</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                                 <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>Properties permit the deployment and management of arbitrary controlled values, within
                                             OSCAL objects. A property can be included for any purpose useful to an application
                                             or implementation. Typically, properties will be used to sort, filter, select, order,
                                             and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                             an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                             lexical composition of properties may be constrained by external processes to ensure
                                             consistency.</p>
                                          <p>Property allows for associated remarks that describe why the specific property value
                                             was applied to the containing object, or the significance of the value in the context
                                             of the containing object.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/assessment-assets/assessment-platforms/links" class="toc3 name">link</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-assets/assessment-platform/link">Switch to XML</a></div>
                                 <p class="formal-name">Link</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                             a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                                          <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition define-assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/assessment-assets/assessment-platforms/uses-components" class="toc3 name">uses-component</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-assets/assessment-platform/uses-component">Switch to XML</a></div>
                                 <p class="formal-name">Uses Component</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> The set of components that are used by the assessment platform.</p>
                                 <p><span class="usa-tag">group as</span> <code class="name">uses-components</code></p>
                                 <details>
                                    <summary>Constraint (1)</summary>
                                    
                                    <div class="constraint">
                                       <p><span class="usa-tag">is unique</span> for <code class="path">responsible-party</code>: any target value must be unique (i.e., occur only once)</p>
                                    </div>
                                    </details>
                                 <details open="open">
                                    <summary>Properties (5)</summary>
                                    <div class="model assembly-model">
                                       <div class="model-entry definition define-flag">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-assessment-common/assessment-assets/assessment-platforms/uses-components/component-uuid" class="toc4 name">component-uuid</h4>
                                             <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                                             <p class="occurrence">[0 or 1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-assets/assessment-platform/uses-component/component-uuid">Switch to XML</a></div>
                                             <p class="formal-name">Component Universally Unique Identifier Reference</p>
                                          </div>
                                          <div class="body">
                                             <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a> identifier reference to a component that is implemented as part of an inventory item.</p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition assembly">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-assessment-common/assessment-assets/assessment-platforms/uses-components/props" class="toc4 name">property</h4>
                                             <p class="type">assembly<br class="br" /> </p>
                                             <p class="occurrence">[0 to ∞]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-assets/assessment-platform/uses-component/prop">Switch to XML</a></div>
                                             <p class="formal-name">Property</p>
                                          </div>
                                          <div class="body">
                                             <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                                             <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                                             <div class="remarks-group usa-prose">
                                                <details open="open">
                                                   <summary class="subhead">Remarks</summary>
                                                   <div class="remarks">
                                                      <p>Properties permit the deployment and management of arbitrary controlled values, within
                                                         OSCAL objects. A property can be included for any purpose useful to an application
                                                         or implementation. Typically, properties will be used to sort, filter, select, order,
                                                         and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                                         an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                                         lexical composition of properties may be constrained by external processes to ensure
                                                         consistency.</p>
                                                      <p>Property allows for associated remarks that describe why the specific property value
                                                         was applied to the containing object, or the significance of the value in the context
                                                         of the containing object.</p>
                                                   </div>
                                                </details>
                                             </div>
                                             <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition assembly">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-assessment-common/assessment-assets/assessment-platforms/uses-components/links" class="toc4 name">link</h4>
                                             <p class="type">assembly<br class="br" /> </p>
                                             <p class="occurrence">[0 to ∞]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-assets/assessment-platform/uses-component/link">Switch to XML</a></div>
                                             <p class="formal-name">Link</p>
                                          </div>
                                          <div class="body">
                                             <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                                             <div class="remarks-group usa-prose">
                                                <details open="open">
                                                   <summary class="subhead">Remarks</summary>
                                                   <div class="remarks">
                                                      <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                                         a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                                                      <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                                                   </div>
                                                </details>
                                             </div>
                                             <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition assembly">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-assessment-common/assessment-assets/assessment-platforms/uses-components/responsible-parties" class="toc4 name">responsible-party</h4>
                                             <p class="type">assembly<br class="br" /> </p>
                                             <p class="occurrence">[0 to ∞]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-assets/assessment-platform/uses-component/responsible-party">Switch to XML</a></div>
                                             <p class="formal-name">Responsible Party</p>
                                          </div>
                                          <div class="body">
                                             <p><span class="usa-tag">group as</span> <code class="name">responsible-parties</code></p>
                                             <p class="definition-link"><a href="#/assembly/oscal-metadata/responsible-party">See definition</a></p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition field">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-assessment-common/assessment-assets/assessment-platforms/uses-components/remarks" class="toc4 name">remarks</h4>
                                             <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                             <p class="occurrence">[0 or 1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-assets/assessment-platform/uses-component/remarks">Switch to XML</a></div>
                                             <p class="formal-name">Remarks</p>
                                          </div>
                                          <div class="body">
                                             <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                                          </div>
                                       </div>
                                    </div>
                                 </details>
                              </div>
                           </div>
                           <div class="model-entry definition field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/assessment-assets/assessment-platforms/remarks" class="toc3 name">remarks</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-assets/assessment-platform/remarks">Switch to XML</a></div>
                                 <p class="formal-name">Remarks</p>
                              </div>
                              <div class="body">
                                 <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-assessment-common/assessment-method" class="toc1 name">assessment-method</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-method">Switch to XML</a></div>
         <p class="formal-name">Assessment Method</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A local definition of a control objective. Uses catalog syntax for control objective
            and assessment activities.</p>
         <details open="open">
            <summary>Properties (6)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-method/uuid" class="toc2 name">uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-method/uuid">Switch to XML</a></div>
                     <p class="formal-name">Assessment Method Universally Unique Identifier</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this assessment method elsewhere in <a href="/concepts/identifier-use/#scope">this or other OSCAL instances</a>. The locally defined <em>UUID</em> of the <code>assessment method</code> can be used to reference the data item locally or globally (e.g., in an imported
                        OSCAL instance). This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                        of the document.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-method/description" class="toc2 name">description</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-method/description">Switch to XML</a></div>
                     <p class="formal-name">Assessment Method Description</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A human-readable description of this assessment method.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-method/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-method/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-method/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-method/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-method/part" class="toc2 name">assessment-part</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-method/part">Switch to XML</a></div>
                     <p class="formal-name">Assessment Part</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">part</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>A <code>part</code> provides for logical partitioning of prose, and can be thought of as a grouping structure
                                 (e.g., section). A <code>part</code> can have child parts allowing for arbitrary nesting of prose content (e.g., statement
                                 hierarchy). A <code>part</code> can contain <code>prop</code> objects that allow for enriching prose text with structured name/value information.</p>
                              <p>A <code>part</code> can be assigned an optional <code>id</code>, which allows for internal and external references to the textual concept contained
                                 within a <code>part</code>. A <code>id</code> provides a means for an OSCAL profile, or a higher layer OSCAL model to reference
                                 a specific part within a <code>catalog</code>. For example, an <code>id</code> can be used to reference or to make modifications to a control statement in a profile.</p>
                              <p>Use of <code>part</code> and <code>prop</code> provides for a wide degree of extensibility within the OSCAL catalog model. The optional
                                 <code>ns</code> provides a means to qualify a part's <code>name</code>, allowing for organization-specific vocabularies to be defined with clear semantics.
                                 Any organization that extends OSCAL in this way should consistently assign a <code>ns</code> value that represents the organization, making a given namespace qualified <code>name</code> unique to that organization. This allows the combination of <code>ns</code> and <code>name</code> to always be unique and unambiguous, even when mixed with extensions from other organizations.
                                 Each organization is responsible for governance of their own extensions, and is strongly
                                 encouraged to publish their extensions as standards to their user community. If no
                                 <code>ns</code> is provided, the name is expected to be in the "OSCAL" namespace.</p>
                              <p>To ensure a <code>ns</code> is unique to an organization and naming conflicts are avoided, a URI containing a
                                 DNS or other globally defined organization name should be used. For example, if FedRAMP
                                 and DoD both extend OSCAL, FedRAMP will use the <code>ns</code> "https://fedramp.gov", while DoD will use the <code>ns</code> "https://defense.gov" for any organization specific <code>name</code>.</p>
                              <p>Tools that process OSCAL content are not required to interpret unrecognized OSCAL
                                 extensions; however, OSCAL compliant tools should not modify or remove unrecognized
                                 extensions, unless there is a compelling reason to do so, such as data sensitivity.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-assessment-common/assessment-part">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-method/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-method/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-ar/assessment-results" class="toc1 name">assessment-results</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/assessment-results">Switch to XML</a></div>
         <p class="formal-name">Security Assessment Results (SAR)</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Security assessment results, such as those provided by a FedRAMP assessor in the
            FedRAMP Security Assessment Report.</p>
         <p><span class="usa-tag">root name</span> <code class="name">assessment-results</code></p>
         <details open="open">
            <summary>Properties (6)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/assessment-results/uuid" class="toc2 name">uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/assessment-results/uuid">Switch to XML</a></div>
                     <p class="formal-name">Assessment Results Universally Unique Identifier</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this assessment results instance in <a href="/concepts/identifier-use/#ar-identifiers">this or other OSCAL instances</a>. The locally defined <em>UUID</em> of the <code>assessment result</code> can be used to reference the data item locally or globally (e.g., in an imported
                        OSCAL instance). This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                        of the document.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/assessment-results/metadata" class="toc2 name">metadata</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/assessment-results/metadata">Switch to XML</a></div>
                     <p class="formal-name">Publication metadata</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/metadata">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/assessment-results/import-ap" class="toc2 name">import-ap</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/assessment-results/import-ap">Switch to XML</a></div>
                     <p class="formal-name">Import Assessment Plan</p>
                  </div>
                  <div class="body">
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Used by the SAR to import information about the original plan for assessing the system.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-ar/import-ap">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/assessment-results/local-definitions" class="toc2 name">local-definitions</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/assessment-results/local-definitions">Switch to XML</a></div>
                     <p class="formal-name">Local Definitions</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Used to define data objects that are used in the assessment plan, that do not appear
                        in the referenced SSP.</p>
                     <details open="open">
                        <summary>Properties (3)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-ar/assessment-results/local-definitions/objectives-and-methods" class="toc3 name">objectives-and-methods</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/assessment-results/local-definitions/objectives-and-methods">Switch to XML</a></div>
                                 <p class="formal-name">Assessment-Specific Control Objective</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">use name</span> <code class="name">objectives-and-methods</code></p>
                                 <p><span class="usa-tag">group as</span> <code class="name">objectives-and-methods</code></p>
                                 <p class="definition-link"><a href="#/assembly/oscal-assessment-common/local-objective">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-ar/assessment-results/local-definitions/activities" class="toc3 name">activity</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/assessment-results/local-definitions/activity">Switch to XML</a></div>
                                 <p class="formal-name">Activity</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">use name</span> <code class="name">activity</code></p>
                                 <p><span class="usa-tag">group as</span> <code class="name">activities</code></p>
                                 <p class="definition-link"><a href="#/assembly/oscal-assessment-common/activity">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-ar/assessment-results/local-definitions/remarks" class="toc3 name">remarks</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/assessment-results/local-definitions/remarks">Switch to XML</a></div>
                                 <p class="formal-name">Remarks</p>
                              </div>
                              <div class="body">
                                 <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/assessment-results/results" class="toc2 name">result</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[1 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/assessment-results/result">Switch to XML</a></div>
                     <p class="formal-name">Assessment Result</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">result</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">results</code></p>
                     <p class="definition-link"><a href="#/assembly/oscal-ar/result">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/assessment-results/back-matter" class="toc2 name">back-matter</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/assessment-results/back-matter">Switch to XML</a></div>
                     <p class="formal-name">Back matter</p>
                  </div>
                  <div class="body">
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Provides a collection of identified <code>resource</code> objects that can be referenced by a <code>link</code> with a <code>rel</code> value of "reference" and an <code>href</code> value that is a fragment "#" followed by a reference to a reference identifier. Other
                                 specialized link "rel" values also use this pattern when indicated in that context
                                 of use.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/back-matter">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-assessment-common/assessment-subject" class="toc1 name">assessment-subject</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-subject">Switch to XML</a></div>
         <p class="formal-name">Subject of Assessment</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Identifies system elements being assessed, such as components, inventory items, and
            locations. In the assessment plan, this identifies a planned assessment subject. In
            the assessment results this is an actual assessment subject, and reflects any changes
            from the plan. exactly what will be the focus of this assessment. Any subjects not
            identified in this way are out-of-scope.</p>
         <div class="remarks-group usa-prose">
            <details open="open">
               <summary class="subhead">Remarks</summary>
               <div class="remarks">
                  <p>Processing of an include/exclude pair starts with processing the include, then removing
                     matching entries in the exclude.</p>
               </div>
            </details>
         </div>
         <details open="open">
            <summary>Properties (7)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-subject/type" class="toc2 name">type</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-subject/type">Switch to XML</a></div>
                     <p class="formal-name">Subject Type</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Indicates the type of assessment subject, such as a component, inventory, item, location,
                        or party represented by this selection statement.</p>
                     <details>
                        <summary>Constraint (1)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span></p>
                           <p>The value <b>may be locally defined</b>, or one of the following:</p>
                           <ul>
                              
                              <li><strong>component</strong>: The referenced assessment subject is a component defined in the SSP, or in the local-definitions
                                 of an Assessment Plan or Assessment Results.</li>
                              
                              <li><strong>inventory-item</strong>: The referenced assessment subject is a inventory item defined in the SSP, or in
                                 the local-definitions of an Assessment Plan or Assessment Results.</li>
                              
                              <li><strong>location</strong>: The referenced assessment subject is a location defined in the metadata of the SSP,
                                 Assessment Plan, or Assessment Results.</li>
                              
                              <li><strong>party</strong>: The referenced assessment subject is a person or team to interview, who is defined
                                 as a party in the metadata of the SSP, Assessment Plan, or Assessment Results.</li>
                              
                              <li><strong>user</strong>: The referenced assessment subject is a user defined in the SSP, or in the local-definitions
                                 of an Assessment Plan or Assessment Results.</li>
                              </ul>
                        </div>
                        </details>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-subject/description" class="toc2 name">description</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-subject/description">Switch to XML</a></div>
                     <p class="formal-name">Include Subjects Description</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A human-readable description of the collection of subjects being included in this
                        assessment.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-subject/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-subject/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-subject/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-subject/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-subject/include-all" class="toc2 name">include-all</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-subject/include-all">Switch to XML</a></div>
                     <p class="formal-name">Include All</p>
                  </div>
                  <div class="body">
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>This element provides an alternative to calling controls individually from a catalog.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-catalog-common/include-all">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-subject/include-subjects" class="toc2 name">include-subject</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[1 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-subject/include-subject">Switch to XML</a></div>
                     <p class="formal-name">Select Assessment Subject</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">include-subject</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">include-subjects</code></p>
                     <p class="definition-link"><a href="#/assembly/oscal-assessment-common/select-subject-by-id">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-subject/exclude-subjects" class="toc2 name">exclude-subject</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-subject/exclude-subject">Switch to XML</a></div>
                     <p class="formal-name">Select Assessment Subject</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">exclude-subject</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">exclude-subjects</code></p>
                     <p class="definition-link"><a href="#/assembly/oscal-assessment-common/select-subject-by-id">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-subject/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-subject/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-assessment-common/assessment-subject-placeholder" class="toc1 name">assessment-subject-placeholder</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-subject-placeholder">Switch to XML</a></div>
         <p class="formal-name">Assessment Subject Placeholder</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Used when the assessment subjects will be determined as part of one or more other
            assessment activities. These assessment subjects will be recorded in the assessment
            results in the assessment log.</p>
         <details open="open">
            <summary>Properties (6)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-subject-placeholder/uuid" class="toc2 name">uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-subject-placeholder/uuid">Switch to XML</a></div>
                     <p class="formal-name">Assessment Subject Placeholder Universally Unique Identifier</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier for a set of assessment subjects that will be identified by a task or
                        an activity that is part of a task. The locally defined <em>UUID</em> of the <code>assessment subject placeholder</code> can be used to reference the data item locally or globally (e.g., in an <a href="/concepts/identifier-use/#scope">imported OSCAL instance</a>). This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                        of the document.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-subject-placeholder/description" class="toc2 name">description</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-subject-placeholder/description">Switch to XML</a></div>
                     <p class="formal-name">Assessment Subject Placeholder Description</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A human-readable description of intent of this assessment subject placeholder.</p>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-subject-placeholder/sources" class="toc2 name">source</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[1 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-subject-placeholder/source">Switch to XML</a></div>
                     <p class="formal-name">Assessment Subject Source</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Assessment subjects will be identified while conducting the referenced activity-instance.</p>
                     <p><span class="usa-tag">group as</span> <code class="name">sources</code></p>
                     <details open="open">
                        <summary>Property (1)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition define-flag">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/assessment-subject-placeholder/sources/task-uuid" class="toc3 name">task-uuid</h3>
                                 <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-subject-placeholder/source/task-uuid">Switch to XML</a></div>
                                 <p class="formal-name">Task Universally Unique Identifier</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference (in this or other OSCAL instances) an assessment
                                    activity to be performed as part of the event. The locally defined <em>UUID</em> of the <code>task</code> can be used to reference the data item locally or globally (e.g., in an <a href="/concepts/identifier-use/#scope">imported OSCAL instance</a>). This UUID should be assigned <em>per-subject</em>, which means it should be consistently used to identify the same subject across revisions
                                    of the document.</p>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-subject-placeholder/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-subject-placeholder/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-subject-placeholder/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-subject-placeholder/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-subject-placeholder/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-subject-placeholder/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-implementation-common/authorized-privilege" class="toc1 name">authorized-privilege</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/authorized-privilege">Switch to XML</a></div>
         <p class="formal-name">Privilege</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Identifies a specific system privilege held by the user, along with an associated
            description and/or rationale for the privilege.</p>
         <details open="open">
            <summary>Properties (3)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/authorized-privilege/title" class="toc2 name">title</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/authorized-privilege/title">Switch to XML</a></div>
                     <p class="formal-name">Privilege Title</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A human readable name for the privilege.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/authorized-privilege/description" class="toc2 name">description</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/authorized-privilege/description">Switch to XML</a></div>
                     <p class="formal-name">Privilege Description</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A summary of the privilege's purpose within the system.</p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/authorized-privilege/functions-performed" class="toc2 name">function-performed</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[1 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/authorized-privilege/function-performed">Switch to XML</a></div>
                     <p class="formal-name">Functions Performed</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">functions-performed</code></p>
                     <p class="definition-link"><a href="#/field/oscal-implementation-common/function-performed">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-metadata/back-matter" class="toc1 name">back-matter</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/back-matter">Switch to XML</a></div>
         <p class="formal-name">Back matter</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A collection of resources, which may be included directly or by reference.</p>
         <div class="remarks-group usa-prose">
            <details open="open">
               <summary class="subhead">Remarks</summary>
               <div class="remarks">
                  <p>Provides a collection of identified <code>resource</code> objects that can be referenced by a <code>link</code> with a <code>rel</code> value of "reference" and an <code>href</code> value that is a fragment "#" followed by a reference to a reference identifier. Other
                     specialized link "rel" values also use this pattern when indicated in that context
                     of use.</p>
               </div>
            </details>
         </div>
         <details>
            <summary>Constraint (1)</summary>
            
            <div class="constraint">
               <p><span class="usa-tag">index</span> for <code class="path">resource</code> an index <code>index-back-matter-resource</code> shall list values returned by targets <code>resource</code> using keys constructed of key field(s) <code>@uuid</code></p>
            </div>
            </details>
         <details open="open">
            <summary>Property (1)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/back-matter/resources" class="toc2 name">resource</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/back-matter/resource">Switch to XML</a></div>
                     <p class="formal-name">Resource</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A resource associated with content in the containing document. A resource may be
                        directly included in the document base64 encoded or may point to one or more equivalent
                        internet resources.</p>
                     <p><span class="usa-tag">group as</span> <code class="name">resources</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>A resource can be used in two ways. 1) it may point to an specific retrievable network
                                 resource using a <code>rlink</code>, or 2) it may be included as an attachment using a <code>base64</code>. A resource may contain multiple <code>rlink</code> and <code>base64</code> entries that represent alternative download locations (rlink) and attachments (base64)
                                 for the same resource. Both rlink and base64 allow for a <code>media-type</code> to be specified, which is used to distinguish between different representations of
                                 the same resource (e.g., Microsoft Word, PDF). When multiple <code>rlink</code> and <code>base64</code> items are included for a given resource, all items must contain equivalent information.
                                 This allows the document consumer to choose a preferred item to process based on a
                                 the selected item's <code>media-type</code>. This is extremely important when the items represent OSCAL content that is represented
                                 in alternate formats (i.e., XML, JSON, YAML), allowing the same OSCAL data to be processed
                                 from any of the available formats indicated by the items.</p>
                              <p>When a resource includes a citation, then the <code>title</code> and <code>citation</code> properties must both be included.</p>
                           </div>
                        </details>
                     </div>
                     <details>
                        <summary>Constraints (6)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">prop/@name</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>type</strong>: Identifies the type of resource represented.</li>
                              
                              <li><strong>version</strong>: For resources representing a published document, this represents the version number
                                 of that document.</li>
                              
                              <li><strong>published</strong>: For resources representing a published document, this represents the publication
                                 date of that document.</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">matches</span> for <code class="path">prop[has-oscal-namespace('http://csrc.nist.gov/ns/oscal') and @name='published']/@value</code>: the target value must match the lexical form of the 'dateTime' data type.</p>
                        </div>
                        
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">prop[@name='type']/@value</code></p>
                           <p>The value <b>may be locally defined</b>, or one of the following:</p>
                           <ul>
                              
                              
                              <li><strong>logo</strong>: Indicates the resource is an organization's logo.</li>
                              
                              <li><strong>image</strong>: Indicates the resource represents an image.</li>
                              
                              <li><strong>screen-shot</strong>: Indicates the resource represents an image of screen content. </li>
                              
                              <li><strong>law</strong>: Indicates the resource represents an applicable law.</li>
                              
                              <li><strong>regulation</strong>: Indicates the resource represents an applicable regulation.</li>
                              
                              <li><strong>standard</strong>: Indicates the resource represents an applicable standard.</li>
                              
                              <li><strong>external-guidance</strong>: Indicates the resource represents applicable guidance.</li>
                              
                              <li><strong>acronyms</strong>: Indicates the resource provides a list of relevant acronyms.</li>
                              
                              <li><strong>citation</strong>: Indicates the resource cites relevant information.</li>
                              
                              
                              <li><strong>policy</strong>: Indicates the resource is a policy.</li>
                              
                              <li><strong>procedure</strong>: Indicates the resource is a procedure.</li>
                              
                              <li><strong>system-guide</strong>: Indicates the resource is guidance document related to the subject system of an
                                 SSP.</li>
                              
                              <li><strong>users-guide</strong>: Indicates the resource is guidance document a user's guide or administrator's guide.</li>
                              
                              <li><strong>administrators-guide</strong>: Indicates the resource is guidance document a administrator's guide.</li>
                              
                              <li><strong>rules-of-behavior</strong>: Indicates the resource represents rules of behavior content.</li>
                              
                              <li><strong>plan</strong>: Indicates the resource represents a plan.</li>
                              
                              
                              <li><strong>artifact</strong>: Indicates the resource represents an artifact, such as may be reviewed by an assessor.</li>
                              
                              <li><strong>evidence</strong>: Indicates the resource represents evidence, such as to support an assessment findiing.</li>
                              
                              <li><strong>tool-output</strong>: Indicates the resource represents output from a tool.</li>
                              
                              <li><strong>raw-data</strong>: Indicates the resource represents machine data, which may require a tool or analysis
                                 for interpretation or presentation.</li>
                              
                              <li><strong>interview-notes</strong>: Indicates the resource represents notes from an interview, such as may be collected
                                 during an assessment.</li>
                              
                              <li><strong>questionnaire</strong>: Indicates the resource is a set of questions, possibly with responses.</li>
                              
                              <li><strong>report</strong>: Indicates the resource is a report.</li>
                              
                              <li><strong>agreement</strong>: Indicates the resource is a formal agreement between two or more parties.</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">has cardinality</span> for <code class="path">rlink|base64</code> the cardinality of  <code>rlink|base64</code> is constrained: <b>1</b>; maximum <b>unbounded</b>.</p>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">is unique</span> for <code class="path">rlink</code>: any target value must be unique (i.e., occur only once)</p>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">is unique</span> for <code class="path">base64</code>: any target value must be unique (i.e., occur only once)</p>
                        </div>
                        
                        A title is required when a citation is provided.
                        
                        </details>
                     <details open="open">
                        <summary>Properties (9)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition define-flag">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-metadata/back-matter/resources/uuid" class="toc3 name">uuid</h3>
                                 <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/back-matter/resource/uuid">Switch to XML</a></div>
                                 <p class="formal-name">Resource Universally Unique Identifier</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this defined resource elsewhere in <a href="/concepts/identifier-use/#scope">this or other OSCAL instances</a>. This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                                    of the document.</p>
                              </div>
                           </div>
                           <div class="model-entry definition define-field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-metadata/back-matter/resources/title" class="toc3 name">title</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/back-matter/resource/title">Switch to XML</a></div>
                                 <p class="formal-name">Resource Title</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A name given to the resource, which may be used by a tool for display and navigation.</p>
                              </div>
                           </div>
                           <div class="model-entry definition define-field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-metadata/back-matter/resources/description" class="toc3 name">description</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/back-matter/resource/description">Switch to XML</a></div>
                                 <p class="formal-name">Resource Description</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A short summary of the resource used to indicate the purpose of the resource.</p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-metadata/back-matter/resources/props" class="toc3 name">property</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/back-matter/resource/prop">Switch to XML</a></div>
                                 <p class="formal-name">Property</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                                 <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>Properties permit the deployment and management of arbitrary controlled values, within
                                             OSCAL objects. A property can be included for any purpose useful to an application
                                             or implementation. Typically, properties will be used to sort, filter, select, order,
                                             and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                             an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                             lexical composition of properties may be constrained by external processes to ensure
                                             consistency.</p>
                                          <p>Property allows for associated remarks that describe why the specific property value
                                             was applied to the containing object, or the significance of the value in the context
                                             of the containing object.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-metadata/back-matter/resources/document-ids" class="toc3 name">document-id</h3>
                                 <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/back-matter/resource/document-id">Switch to XML</a></div>
                                 <p class="formal-name">Document Identifier</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">group as</span> <code class="name">document-ids</code></p>
                                 <p><span class="usa-tag">value key</span> <code class="name">identifier</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>This element is optional, but it will always have a valid value, as if it is missing
                                             the value of "document-id" is assumed to be equal to the UUID of the root. This requirement
                                             allows for document creators to retroactively link an update to the original version,
                                             by providing a document-id on the new document that is equal to the uuid of the original
                                             document.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/field/oscal-metadata/document-id">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition define-assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-metadata/back-matter/resources/citation" class="toc3 name">citation</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/back-matter/resource/citation">Switch to XML</a></div>
                                 <p class="formal-name">Citation</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A citation consisting of end note text and optional structured bibliographic data.</p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>The <code>text</code> is used to define the endnote text, without any required bibliographic structure.
                                             If structured bibliographic data is needed, then the <code>biblio</code> can be used for this purpose.</p>
                                          <p>A <code>biblio</code> can be used to capture a structured bibliographical citation in an appropriate format.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <details open="open">
                                    <summary>Properties (3)</summary>
                                    <div class="model assembly-model">
                                       <div class="model-entry definition define-field">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-metadata/back-matter/resources/citation/text" class="toc4 name">text</h4>
                                             <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                                             <p class="occurrence">[1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/back-matter/resource/citation/text">Switch to XML</a></div>
                                             <p class="formal-name">Citation Text</p>
                                          </div>
                                          <div class="body">
                                             <p class="description"><span class="usa-tag">description</span> A line of citation text.</p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition assembly">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-metadata/back-matter/resources/citation/props" class="toc4 name">property</h4>
                                             <p class="type">assembly<br class="br" /> </p>
                                             <p class="occurrence">[0 to ∞]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/back-matter/resource/citation/prop">Switch to XML</a></div>
                                             <p class="formal-name">Property</p>
                                          </div>
                                          <div class="body">
                                             <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                                             <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                                             <div class="remarks-group usa-prose">
                                                <details open="open">
                                                   <summary class="subhead">Remarks</summary>
                                                   <div class="remarks">
                                                      <p>Properties permit the deployment and management of arbitrary controlled values, within
                                                         OSCAL objects. A property can be included for any purpose useful to an application
                                                         or implementation. Typically, properties will be used to sort, filter, select, order,
                                                         and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                                         an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                                         lexical composition of properties may be constrained by external processes to ensure
                                                         consistency.</p>
                                                      <p>Property allows for associated remarks that describe why the specific property value
                                                         was applied to the containing object, or the significance of the value in the context
                                                         of the containing object.</p>
                                                   </div>
                                                </details>
                                             </div>
                                             <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition assembly">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-metadata/back-matter/resources/citation/links" class="toc4 name">link</h4>
                                             <p class="type">assembly<br class="br" /> </p>
                                             <p class="occurrence">[0 to ∞]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/back-matter/resource/citation/link">Switch to XML</a></div>
                                             <p class="formal-name">Link</p>
                                          </div>
                                          <div class="body">
                                             <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                                             <div class="remarks-group usa-prose">
                                                <details open="open">
                                                   <summary class="subhead">Remarks</summary>
                                                   <div class="remarks">
                                                      <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                                         a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                                                      <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                                                   </div>
                                                </details>
                                             </div>
                                             <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                                          </div>
                                       </div>
                                    </div>
                                 </details>
                              </div>
                           </div>
                           <div class="model-entry definition define-assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-metadata/back-matter/resources/rlinks" class="toc3 name">rlink</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/back-matter/resource/rlink">Switch to XML</a></div>
                                 <p class="formal-name">Resource link</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A pointer to an external resource with an optional hash for verification and change
                                    detection.</p>
                                 <p><span class="usa-tag">group as</span> <code class="name">rlinks</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>This construct is different from <code>link</code>, which makes no provision for a hash or formal title.</p>
                                          <p>Multiple <code>rlink</code> can be included for a resource. In such a case, all provided <code>rlink</code> items are intended to be equivalent in content, but may differ in structure. A <code>media-type</code> is used to identify the format of a given rlink, and can be used to differentiate
                                             a items in a collection of rlinks. The <code>media-type</code> also provides a hint to the OSCAL document consumer about the structure of the resource
                                             referenced by the <code>rlink</code>. </p>
                                       </div>
                                    </details>
                                 </div>
                                 <details open="open">
                                    <summary>Properties (3)</summary>
                                    <div class="model assembly-model">
                                       <div class="model-entry definition define-flag">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-metadata/back-matter/resources/rlinks/href" class="toc4 name">href</h4>
                                             <p class="type"><a href="/reference/datatypes/#uri-reference">uri-reference</a></p>
                                             <p class="occurrence">[0 or 1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/back-matter/resource/rlink/href">Switch to XML</a></div>
                                             <p class="formal-name">Hypertext Reference</p>
                                          </div>
                                          <div class="body">
                                             <p class="description"><span class="usa-tag">description</span> A resolvable URI reference to a resource.</p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition flag">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-metadata/back-matter/resources/rlinks/media-type" class="toc4 name">media-type</h4>
                                             <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                                             <p class="occurrence">[0 or 1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/back-matter/resource/rlink/media-type">Switch to XML</a></div>
                                             <p class="formal-name">Media Type</p>
                                          </div>
                                          <div class="body">
                                             <p class="definition-link"><a href="#/flag/oscal-metadata/media-type">See definition</a></p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition field">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-metadata/back-matter/resources/rlinks/hashes" class="toc4 name">hash</h4>
                                             <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                                             <p class="occurrence">[0 to ∞]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/back-matter/resource/rlink/hash">Switch to XML</a></div>
                                             <p class="formal-name">Hash</p>
                                          </div>
                                          <div class="body">
                                             <p><span class="usa-tag">group as</span> <code class="name">hashes</code></p>
                                             <p><span class="usa-tag">value key</span> <code class="name">value</code></p>
                                             <div class="remarks-group usa-prose">
                                                <details open="open">
                                                   <summary class="subhead">Remarks</summary>
                                                   <div class="remarks">
                                                      <p>A hash value can be used to authenticate that a referenced resource is the same resources
                                                         as was pointed to by the author of the reference.</p>
                                                   </div>
                                                   <div class="remarks">
                                                      <p>When appearing as part of a <code>resource/rlink</code>, the hash applies to the resource referenced by the <code>href</code>. </p>
                                                   </div>
                                                </details>
                                             </div>
                                             <p class="definition-link"><a href="#/field/oscal-metadata/hash">See definition</a></p>
                                          </div>
                                       </div>
                                    </div>
                                 </details>
                              </div>
                           </div>
                           <div class="model-entry definition define-field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-metadata/back-matter/resources/base64" class="toc3 name">base64</h3>
                                 <p class="type"><a href="/reference/datatypes/#base64binary">base64Binary</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/back-matter/resource/base64">Switch to XML</a></div>
                                 <p class="formal-name">Base64</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> The Base64 alphabet in RFC 2045 - aligned with XSD.</p>
                                 <p><span class="usa-tag">value key</span> <code class="name">value</code></p>
                                 <details open="open">
                                    <summary>Properties (3)</summary>
                                    <div class="model field-model">
                                       <div class="model-entry definition define-flag">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-metadata/back-matter/resources/base64/filename" class="toc4 name">filename</h4>
                                             <p class="type"><a href="/reference/datatypes/#uri-reference">uri-reference</a></p>
                                             <p class="occurrence">[0 or 1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/back-matter/resource/base64/filename">Switch to XML</a></div>
                                             <p class="formal-name">File Name</p>
                                          </div>
                                          <div class="body">
                                             <p class="description"><span class="usa-tag">description</span> Name of the file before it was encoded as Base64 to be embedded in a <code>resource</code>. This is the name that will be assigned to the file when the file is decoded.</p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition flag">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-metadata/back-matter/resources/base64/media-type" class="toc4 name">media-type</h4>
                                             <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                                             <p class="occurrence">[0 or 1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/back-matter/resource/base64/media-type">Switch to XML</a></div>
                                             <p class="formal-name">Media Type</p>
                                          </div>
                                          <div class="body">
                                             <p class="definition-link"><a href="#/flag/oscal-metadata/media-type">See definition</a></p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition m:define-flag">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-metadata/back-matter/resources/base64/value" class="toc4 name">value</h4>
                                             <p class="type"><a href="/reference/datatypes/#base64binary">base64Binary</a></p>
                                             <p class="occurrence">[0 or 1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/back-matter/resource/base64">Switch to XML</a></div>
                                             <p class="formal-name">Base64 Value</p>
                                          </div>
                                          <div class="body">
                                             <p class="description"><span class="usa-tag">description</span> This property provides the (nominal) value for this object as a whole.</p>
                                          </div>
                                       </div>
                                    </div>
                                 </details>
                              </div>
                           </div>
                           <div class="model-entry definition field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-metadata/back-matter/resources/remarks" class="toc3 name">remarks</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/back-matter/resource/remarks">Switch to XML</a></div>
                                 <p class="formal-name">Remarks</p>
                              </div>
                              <div class="body">
                                 <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-assessment-common/characterization" class="toc1 name">characterization</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/characterization">Switch to XML</a></div>
         <p class="formal-name">Characterization</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A collection of descriptive data about the containing object from a specific origin.</p>
         <details open="open">
            <summary>Properties (4)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/characterization/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/characterization/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/characterization/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/characterization/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/characterization/origin" class="toc2 name">origin</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/characterization/origin">Switch to XML</a></div>
                     <p class="formal-name">Origin</p>
                  </div>
                  <div class="body">
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>metadata about the specific actor that generated this descriptive data.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-assessment-common/origin">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/characterization/facets" class="toc2 name">facet</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[1 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/characterization/facet">Switch to XML</a></div>
                     <p class="formal-name">Facet</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> An individual characteristic that is part of a larger set produced by the same actor.</p>
                     <p><span class="usa-tag">group as</span> <code class="name">facets</code></p>
                     <details>
                        <summary>Constraints (30)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed value</span> for <code class="path">prop/@name</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>state</strong>: Indicates if the facet is 'initial' as first identified, or 'adjusted' indicating
                                 that the value has be changed after some adjustments have been made (e.g., to identify
                                 residual risk).</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">prop[@name='risk-state']/@value</code></p>
                           <p>The value <b>may be locally defined</b>, or one of the following:</p>
                           <ul>
                              
                              <li><strong>initial</strong>: As first identified.</li>
                              
                              <li><strong>adjusted</strong>: Indicates that residual risk remains after some adjustments have been made.</li>
                              </ul>
                        </div>
                        
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system='http://csrc.nist.gov/oscal']/@name</code></p>
                           <p>The value <b>may be locally defined</b>, or one of the following:</p>
                           <ul>
                              
                              <li><strong>likelihood</strong>: General likelihood rating.</li>
                              
                              <li><strong>impact</strong>: General impact rating.</li>
                              
                              <li><strong>risk</strong>: General risk rating.</li>
                              
                              <li><strong>severity</strong>: General severity rating.</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system='http://fedramp.gov']/@name</code></p>
                           <p>The value <b>may be locally defined</b>, or one of the following:</p>
                           <ul>
                              
                              <li><strong>likelihood</strong>: Likelihood as defined by FedRAMP. The class can be used to specify 'initial' and
                                 'adjusted' risk states.</li>
                              
                              <li><strong>impact</strong>: Impact as defined by FedRAMP. The class can be used to specify 'initial' and 'adjusted'
                                 risk states.</li>
                              
                              <li><strong>risk</strong>: Risk as calculated according to FedRAMP. The class can be used to specify 'initial'
                                 and 'adjusted' risk states.</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed value</span> for <code class="path">(.)[@system='http://cve.mitre.org']/@name</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>cve-id</strong>: An identifier managed by the CVE program (see https://cve.mitre.org/).</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system='http://www.first.org/cvss/v2.0']/@name</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>access-vector</strong>: Base: Access Vector</li>
                              
                              <li><strong>access-complexity</strong>: Base: Access Complexity</li>
                              
                              <li><strong>authentication</strong>: Base: Authentication</li>
                              
                              <li><strong>confidentiality-impact</strong>: Base: Confidentiality Impact</li>
                              
                              <li><strong>integrity-impact</strong>: Base: Integrity Impact</li>
                              
                              <li><strong>availability-impact</strong>: Base: Availability Impact</li>
                              
                              <li><strong>exploitability</strong>: Temporal: Exploitability</li>
                              
                              <li><strong>remediation-level</strong>: Temporal: Remediation Level</li>
                              
                              <li><strong>report-confidence</strong>: Temporal: Report Confidence</li>
                              
                              <li><strong>collateral-damage-potential</strong>: Environmental: Collateral Damage Potential</li>
                              
                              <li><strong>target-distribution</strong>: Environmental: Target Distribution</li>
                              
                              <li><strong>confidentiality-requirement</strong>: Environmental: Confidentiality Requirement</li>
                              
                              <li><strong>integrity-requirement</strong>: Environmental: Integrity Requirement</li>
                              
                              <li><strong>availability-requirement</strong>: Environmental: Availability Requirement</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system='http://www.first.org/cvss/v2.0' and @name='access-vector']/@value</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>local</strong>: Local</li>
                              
                              <li><strong>adjacent-network</strong>: Network Adjacent</li>
                              
                              <li><strong>network</strong>: Network</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system='http://www.first.org/cvss/v2.0' and @name='access-complexity']/@value</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>high</strong>: High</li>
                              
                              <li><strong>medium</strong>: Medium</li>
                              
                              <li><strong>low</strong>: Low</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system='http://www.first.org/cvss/v2.0' and @name='authentication']/@value</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>multiple</strong>: Multiple</li>
                              
                              <li><strong>single</strong>: Single</li>
                              
                              <li><strong>none</strong>: None</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system='http://www.first.org/cvss/v2.0' and @name=('confidentiality-impact',
                                 'integrity-impact', 'availability-impact')]/@value</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>none</strong>: None</li>
                              
                              <li><strong>partial</strong>: Partial</li>
                              
                              <li><strong>complete</strong>: Complete</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system='http://www.first.org/cvss/v2.0' and @name='exploitability']/@value</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>unproven</strong>: Unproven</li>
                              
                              <li><strong>proof-of-concept</strong>: Proof-of-Concept</li>
                              
                              <li><strong>functional</strong>: Functional</li>
                              
                              <li><strong>high</strong>: High</li>
                              
                              <li><strong>not-defined</strong>: Not Defined</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system='http://www.first.org/cvss/v2.0' and @name='remediation-level']/@value</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>official-fix</strong>: Official Fix</li>
                              
                              <li><strong>temporary-fix</strong>: Temporary Fix</li>
                              
                              <li><strong>workaround</strong>: Workaround</li>
                              
                              <li><strong>unavailable</strong>: Unavailable</li>
                              
                              <li><strong>not-defined</strong>: Not Defined</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system='http://www.first.org/cvss/v2.0' and @name='report-confidence']/@value</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>unconfirmed</strong>: Unconfirmed</li>
                              
                              <li><strong>uncorroborated</strong>: Uncorroborated</li>
                              
                              <li><strong>confirmed</strong>: Confirmed</li>
                              
                              <li><strong>not-defined</strong>: Not Defined</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system='http://www.first.org/cvss/v2.0' and @name='collateral-damage-potential']/@value</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>none</strong>: None</li>
                              
                              <li><strong>low</strong>: Low (light loss)</li>
                              
                              <li><strong>low-medium</strong>: Low Medium</li>
                              
                              <li><strong>medium-high</strong>: Medium High</li>
                              
                              <li><strong>high</strong>: High (catastrophic loss)</li>
                              
                              <li><strong>not-defined</strong>: Not Defined</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system='http://www.first.org/cvss/v2.0' and @name=('target-distribution', 'confidentiality-requirement',
                                 'integrity-requirement', 'availability-requirement')]/@value</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>none</strong></li>
                              
                              <li><strong>low</strong></li>
                              
                              <li><strong>medium</strong></li>
                              
                              <li><strong>high</strong></li>
                              
                              <li><strong>not-defined</strong></li>
                              </ul>
                        </div>
                        
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system=('http://www.first.org/cvss/v3.0', 'http://www.first.org/cvss/v3.1')]/@name</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>attack-vector</strong>: Base: Attack Vector</li>
                              
                              <li><strong>access-complexity</strong>: Base: Attack Complexity</li>
                              
                              <li><strong>privileges-required</strong>: Base: Privileges Required</li>
                              
                              <li><strong>user-interaction</strong>: Base: User Interaction</li>
                              
                              <li><strong>scope</strong>: Base: Scope</li>
                              
                              <li><strong>confidentiality-impact</strong>: Base: Confidentiality Impact</li>
                              
                              <li><strong>integrity-impact</strong>: Base: Integrity Impact</li>
                              
                              <li><strong>availability-impact</strong>: Base: Availability Impact</li>
                              
                              <li><strong>exploit-code-maturity</strong>: Temporal: Exploit Code Maturity</li>
                              
                              <li><strong>remediation-level</strong>: Temporal: Remediation Level</li>
                              
                              <li><strong>report-confidence</strong>: Temporal: Report Confidence</li>
                              
                              <li><strong>modified-attack-vector</strong>: Environmental: Modified Attack Vector</li>
                              
                              <li><strong>modified-attack-complexity</strong>: Environmental: Modified Attack Complexity</li>
                              
                              <li><strong>modified-privileges-required</strong>: Environmental: Modified Privileges Required</li>
                              
                              <li><strong>modified-user-interaction</strong>: Environmental: Modified User Interaction</li>
                              
                              <li><strong>modified-scope</strong>: Environmental: Modified Scope</li>
                              
                              <li><strong>modified-confidentiality</strong>: Environmental: Modified Confidentiality</li>
                              
                              <li><strong>modified-integrity</strong>: Environmental: Modified Integrity</li>
                              
                              <li><strong>modified-availability</strong>: Environmental: Modified Availability</li>
                              
                              <li><strong>confidentiality-requirement</strong>: Environmental: Confidentiality Requirement Modifier</li>
                              
                              <li><strong>integrity-requirement</strong>: Environmental: Integrity Requirement Modifier</li>
                              
                              <li><strong>availability-requirement</strong>: Environmental: Availability Requirement Modifier</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system=('http://www.first.org/cvss/v3.0', 'http://www.first.org/cvss/v3.1') and
                                 @name='access-vector']/@value</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>network</strong>: Network</li>
                              
                              <li><strong>adjacent</strong>: Adjacent</li>
                              
                              <li><strong>local</strong>: Local</li>
                              
                              <li><strong>physical</strong>: Physical</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system=('http://www.first.org/cvss/v3.0', 'http://www.first.org/cvss/v3.1') and
                                 @name='access-complexity']/@value</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>high</strong>: High</li>
                              
                              <li><strong>low</strong>: Low</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system=('http://www.first.org/cvss/v3.0', 'http://www.first.org/cvss/v3.1') and
                                 @name=('privileges-required', 'confidentiality-impact', 'integrity-impact', 'availability-impact')]/@value</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>none</strong>: None</li>
                              
                              <li><strong>low</strong>: Low</li>
                              
                              <li><strong>high</strong>: High</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system=('http://www.first.org/cvss/v3.0', 'http://www.first.org/cvss/v3.1') and
                                 @name='user-interaction']/@value</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>none</strong>: None</li>
                              
                              <li><strong>required</strong>: Required</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system=('http://www.first.org/cvss/v3.0', 'http://www.first.org/cvss/v3.1') and
                                 @name='scope']/@value</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>unchanged</strong>: Unchanged</li>
                              
                              <li><strong>changed</strong>: Changed</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system=('http://www.first.org/cvss/v3.0', 'http://www.first.org/cvss/v3.1') and
                                 @name='exploit-code-maturity']/@value</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>not-defined</strong>: Not Defined</li>
                              
                              <li><strong>unproven</strong>: Unproven</li>
                              
                              <li><strong>proof-of-concept</strong>: Proof-of-Concept</li>
                              
                              <li><strong>functional</strong>: Functional</li>
                              
                              <li><strong>high</strong>: High</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system=('http://www.first.org/cvss/v3.0', 'http://www.first.org/cvss/v3.1') and
                                 @name='remediation-level']/@value</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>not-defined</strong>: Not Defined</li>
                              
                              <li><strong>official-fix</strong>: Official Fix</li>
                              
                              <li><strong>temporary-fix</strong>: Temporary Fix</li>
                              
                              <li><strong>workaround</strong>: Workaround</li>
                              
                              <li><strong>unavailable</strong>: Unavailable</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system=('http://www.first.org/cvss/v3.0', 'http://www.first.org/cvss/v3.1') and
                                 @name='report-confidence']/@value</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>not-defined</strong>: Not Defined</li>
                              
                              <li><strong>unknown</strong>: Unknown</li>
                              
                              <li><strong>reasonable</strong>: Reasonable</li>
                              
                              <li><strong>confirmed</strong>: Confirmed</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system=('http://www.first.org/cvss/v3.0', 'http://www.first.org/cvss/v3.1') and
                                 @name=('confidentiality-requirement', 'integrity-requirement', 'availability-requirement')]/@value</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>not-defined</strong>: Not Defined</li>
                              
                              <li><strong>low</strong>: Low</li>
                              
                              <li><strong>medium</strong>: Medium</li>
                              
                              <li><strong>high</strong>: High</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system=('http://www.first.org/cvss/v3.0', 'http://www.first.org/cvss/v3.1') and
                                 @name='modified-attack-vector']/@value</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>not-defined</strong>: Not Defined</li>
                              
                              <li><strong>network</strong>: Network</li>
                              
                              <li><strong>adjacent</strong>: Adjacent</li>
                              
                              <li><strong>local</strong>: Local</li>
                              
                              <li><strong>physical</strong>: Physical</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system=('http://www.first.org/cvss/v3.0', 'http://www.first.org/cvss/v3.1') and
                                 @name='modified-attack-complexity']/@value</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>not-defined</strong>: Not Defined</li>
                              
                              <li><strong>high</strong>: High</li>
                              
                              <li><strong>low</strong>: Low</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system=('http://www.first.org/cvss/v3.0', 'http://www.first.org/cvss/v3.1') and
                                 @name=('modified-privileges-required', 'modified-confidentiality', 'modified-integrity',
                                 'modified-availability')]/@value</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>not-defined</strong>: Not Defined</li>
                              
                              <li><strong>none</strong>: None</li>
                              
                              <li><strong>low</strong>: Low</li>
                              
                              <li><strong>high</strong>: High</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system=('http://www.first.org/cvss/v3.0', 'http://www.first.org/cvss/v3.1') and
                                 @name='modified-user-interaction']/@value</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>not-defined</strong>: Not Defined</li>
                              
                              <li><strong>none</strong>: None</li>
                              
                              <li><strong>required</strong>: Required</li>
                              </ul>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@system=('http://www.first.org/cvss/v3.0', 'http://www.first.org/cvss/v3.1') and
                                 @name='modified-scope']/@value</code></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>not-defined</strong>: Not Defined</li>
                              
                              <li><strong>unchanged</strong>: Unchanged</li>
                              
                              <li><strong>changed</strong>: Changed</li>
                              </ul>
                        </div>
                        </details>
                     <details open="open">
                        <summary>Properties (6)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition define-flag">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/characterization/facets/name" class="toc3 name">name</h3>
                                 <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/characterization/facet/name">Switch to XML</a></div>
                                 <p class="formal-name">Facet Name</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> The name of the risk metric within the specified system.</p>
                              </div>
                           </div>
                           <div class="model-entry definition define-flag">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/characterization/facets/system" class="toc3 name">system</h3>
                                 <p class="type"><a href="/reference/datatypes/#uri">uri</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/characterization/facet/system">Switch to XML</a></div>
                                 <p class="formal-name">Naming System</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> Specifies the naming system under which this risk metric is organized, which allows
                                    for the same names to be used in different systems controlled by different parties.
                                    This avoids the potential of a name clash.</p>
                                 <details>
                                    <summary>Constraint (1)</summary>
                                    
                                    <div class="constraint">
                                       <p><span class="usa-tag">allowed values</span></p>
                                       <p>The value <b>may be locally defined</b>, or one of the following:</p>
                                       <ul>
                                          
                                          <li><strong>http://fedramp.gov</strong></li>
                                          
                                          <li><strong>http://csrc.nist.gov/ns/oscal</strong></li>
                                          
                                          <li><strong>http://csrc.nist.gov/ns/oscal/unknown</strong>: The facet is from an unknown taxonomy. The meaning of the name is tool or organization
                                             specific.</li>
                                          
                                          <li><strong>http://cve.mitre.org</strong></li>
                                          
                                          
                                          <li><strong>http://www.first.org/cvss/v2.0</strong></li>
                                          
                                          <li><strong>http://www.first.org/cvss/v3.0</strong></li>
                                          
                                          <li><strong>http://www.first.org/cvss/v3.1</strong></li>
                                          </ul>
                                    </div>
                                    </details>
                              </div>
                           </div>
                           <div class="model-entry definition define-flag">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/characterization/facets/value" class="toc3 name">value</h3>
                                 <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/characterization/facet/value">Switch to XML</a></div>
                                 <p class="formal-name">Facet Value</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> Indicates the value of the facet.</p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/characterization/facets/props" class="toc3 name">property</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/characterization/facet/prop">Switch to XML</a></div>
                                 <p class="formal-name">Property</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                                 <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>Properties permit the deployment and management of arbitrary controlled values, within
                                             OSCAL objects. A property can be included for any purpose useful to an application
                                             or implementation. Typically, properties will be used to sort, filter, select, order,
                                             and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                             an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                             lexical composition of properties may be constrained by external processes to ensure
                                             consistency.</p>
                                          <p>Property allows for associated remarks that describe why the specific property value
                                             was applied to the containing object, or the significance of the value in the context
                                             of the containing object.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/characterization/facets/links" class="toc3 name">link</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/characterization/facet/link">Switch to XML</a></div>
                                 <p class="formal-name">Link</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                             a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                                          <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/characterization/facets/remarks" class="toc3 name">remarks</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/characterization/facet/remarks">Switch to XML</a></div>
                                 <p class="formal-name">Remarks</p>
                              </div>
                              <div class="body">
                                 <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-flag">
      <div class="definition-header">
         <h1 id="/flag/oscal-catalog-common/control-id" class="toc1 name">control-id</h1>
         <p class="type"><a href="/reference/datatypes/#token">token</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/flag/oscal-catalog-common/control-id">Switch to XML</a></div>
         <p class="formal-name">Control Identifier Reference</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#human-oriented">human-oriented</a> identifier reference to a control with a corresponding <code>id</code> value. When referencing an externally defined <code>control</code>, the <code>Control Identifier Reference</code> must be used in the context of the external / imported OSCAL instance (e.g., uri-reference).</p>
      </div>
   </div>
   <div class="model-entry definition define-field">
      <div class="definition-header">
         <h1 id="/field/oscal-metadata/document-id" class="toc1 name">document-id</h1>
         <p class="type"><a href="/reference/datatypes/#string">string</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-metadata/document-id">Switch to XML</a></div>
         <p class="formal-name">Document Identifier</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A document identifier qualified by an identifier <code>scheme</code>. A document identifier provides a <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with a <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that is used for a group of documents that are to be treated as different versions
            of the same document. If this element does not appear, or if the value of this element
            is empty, the value of "document-id" is equal to the value of the "uuid" flag of the
            top-level root element.</p>
         <p><span class="usa-tag">value key</span> <code class="name">identifier</code></p>
         <div class="remarks-group usa-prose">
            <details open="open">
               <summary class="subhead">Remarks</summary>
               <div class="remarks">
                  <p>This element is optional, but it will always have a valid value, as if it is missing
                     the value of "document-id" is assumed to be equal to the UUID of the root. This requirement
                     allows for document creators to retroactively link an update to the original version,
                     by providing a document-id on the new document that is equal to the uuid of the original
                     document.</p>
               </div>
            </details>
         </div>
         <details open="open">
            <summary>Properties (2)</summary>
            <div class="model field-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/field/oscal-metadata/document-id/scheme" class="toc2 name">scheme</h2>
                     <p class="type"><a href="/reference/datatypes/#uri">uri</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-metadata/document-id/scheme">Switch to XML</a></div>
                     <p class="formal-name">Document Identification Scheme</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Qualifies the kind of document identifier using a URI. If the scheme is not provided
                        the value of the element will be interpreted as a string of characters. </p>
                     <details>
                        <summary>Constraint (1)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed value</span></p>
                           <p>The value <b>may be locally defined</b>, or the following:</p>
                           <ul>
                              
                              <li><strong>https://www.doi.org/</strong>: A Digital Object Identifier (DOI); use is preferred, since this allows for retrieval
                                 of a full bibliographic record.</li>
                              </ul>
                        </div>
                        </details>
                  </div>
               </div>
               <div class="model-entry definition m:define-flag">
                  <div class="instance-header">
                     <h2 id="/field/oscal-metadata/document-id/identifier" class="toc2 name">identifier</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-metadata/document-id">Switch to XML</a></div>
                     <p class="formal-name">Document Identifier Value</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> This property provides the (nominal) value for this object as a whole.</p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-field">
      <div class="definition-header">
         <h1 id="/field/oscal-metadata/email-address" class="toc1 name">email-address</h1>
         <p class="type"><a href="/reference/datatypes/#email">email</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-metadata/email-address">Switch to XML</a></div>
         <p class="formal-name">Email Address</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> An email address as defined by <a href="https://tools.ietf.org/html/rfc5322#section-3.4.1">RFC 5322 Section 3.4.1</a>. </p>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-ar/finding" class="toc1 name">finding</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/finding">Switch to XML</a></div>
         <p class="formal-name">Finding</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Describes an individual finding.</p>
         <details open="open">
            <summary>Properties (11)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/finding/uuid" class="toc2 name">uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/finding/uuid">Switch to XML</a></div>
                     <p class="formal-name">Finding Universally Unique Identifier</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this finding in <a href="/concepts/identifier-use/#ar-identifiers">this or other OSCAL instances</a>. The locally defined <em>UUID</em> of the <code>finding</code> can be used to reference the data item locally or globally (e.g., in an imported
                        OSCAL instance). This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                        of the document.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/finding/title" class="toc2 name">title</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/finding/title">Switch to XML</a></div>
                     <p class="formal-name">Finding Title</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> The title for this finding.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/finding/description" class="toc2 name">description</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/finding/description">Switch to XML</a></div>
                     <p class="formal-name">Finding Description</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A human-readable description of this finding.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/finding/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/finding/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/finding/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/finding/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/finding/origins" class="toc2 name">origin</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/finding/origin">Switch to XML</a></div>
                     <p class="formal-name">Origin</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">origins</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Used to identify the individual and/or tool generated this finding.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-assessment-common/origin">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/finding/target" class="toc2 name">target</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/finding/target">Switch to XML</a></div>
                     <p class="formal-name">Objective Status</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">target</code></p>
                     <p class="definition-link"><a href="#/assembly/oscal-assessment-common/finding-target">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/finding/implementation-statement-uuid" class="toc2 name">implementation-statement-uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/finding/implementation-statement-uuid">Switch to XML</a></div>
                     <p class="formal-name">Implementation Statement UUID</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a> identifier reference to the implementation statement in the SSP to which this finding
                        is related.</p>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/finding/related-observations" class="toc2 name">related-observation</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/finding/related-observation">Switch to XML</a></div>
                     <p class="formal-name">Related Observation</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Relates the finding to a set of referenced observations that were used to determine
                        the finding.</p>
                     <p><span class="usa-tag">group as</span> <code class="name">related-observations</code></p>
                     <details open="open">
                        <summary>Property (1)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition define-flag">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-ar/finding/related-observations/observation-uuid" class="toc3 name">observation-uuid</h3>
                                 <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/finding/related-observation/observation-uuid">Switch to XML</a></div>
                                 <p class="formal-name">Observation Universally Unique Identifier Reference</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a> identifier reference to an observation defined in the list of observations.</p>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/finding/related-risks" class="toc2 name">associated-risk</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/finding/associated-risk">Switch to XML</a></div>
                     <p class="formal-name">Associated Risk</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Relates the finding to a set of referenced risks that were used to determine the
                        finding.</p>
                     <p><span class="usa-tag">group as</span> <code class="name">related-risks</code></p>
                     <details open="open">
                        <summary>Property (1)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition define-flag">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-ar/finding/related-risks/risk-uuid" class="toc3 name">risk-uuid</h3>
                                 <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/finding/associated-risk/risk-uuid">Switch to XML</a></div>
                                 <p class="formal-name">Risk Universally Unique Identifier Reference</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a> identifier reference to a risk defined in the list of risks.</p>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/finding/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/finding/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-assessment-common/finding-target" class="toc1 name">finding-target</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/finding-target">Switch to XML</a></div>
         <p class="formal-name">Objective Status</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Captures an assessor's conclusions regarding the degree to which an objective is
            satisfied.</p>
         <details open="open">
            <summary>Properties (9)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/finding-target/type" class="toc2 name">type</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/finding-target/type">Switch to XML</a></div>
                     <p class="formal-name">Finding Target Type</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Identifies the type of the target.</p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>The target will always be a reference to: 1) a control statement, or 2) a control
                                 objective. In the former case, there is always a single top-level statement within
                                 a control. Thus, if the entire control is targeted, this statement identifier can
                                 be used.</p>
                           </div>
                        </details>
                     </div>
                     <details>
                        <summary>Constraint (1)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>statement-id</strong>: A reference to a control statement identifier within a control.</li>
                              
                              <li><strong>objective-id</strong>: A reference to a control objective identifier within a control.</li>
                              </ul>
                        </div>
                        </details>
                  </div>
               </div>
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/finding-target/target-id" class="toc2 name">target-id</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/finding-target/target-id">Switch to XML</a></div>
                     <p class="formal-name">Finding Target Identifier Reference</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a> identifier reference for a specific target qualified by the <code>type</code>.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/finding-target/title" class="toc2 name">title</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/finding-target/title">Switch to XML</a></div>
                     <p class="formal-name">Objective Status Title</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> The title for this objective status.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/finding-target/description" class="toc2 name">description</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/finding-target/description">Switch to XML</a></div>
                     <p class="formal-name">Objective Status Description</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A human-readable description of the assessor's conclusions regarding the degree to
                        which an objective is satisfied.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/finding-target/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/finding-target/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/finding-target/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/finding-target/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/finding-target/status" class="toc2 name">status</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/finding-target/status">Switch to XML</a></div>
                     <p class="formal-name">Objective Status</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A determination of if the objective is satisfied or not within a given system.</p>
                     <details open="open">
                        <summary>Properties (3)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition define-flag">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/finding-target/status/state" class="toc3 name">state</h3>
                                 <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/finding-target/status/state">Switch to XML</a></div>
                                 <p class="formal-name">Objective Status State</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> An indication as to whether the objective is satisfied or not.</p>
                                 <details>
                                    <summary>Constraint (1)</summary>
                                    
                                    <div class="constraint">
                                       <p><span class="usa-tag">allowed values</span></p>
                                       <p>The value <b>must</b> be one of the following:</p>
                                       <ul>
                                          
                                          <li><strong>satisfied</strong>: The objective has been completely satisfied.</li>
                                          
                                          <li><strong>not-satisfied</strong>: The objective has not been completely satisfied, but may be partially satisfied.</li>
                                          </ul>
                                    </div>
                                    </details>
                              </div>
                           </div>
                           <div class="model-entry definition define-flag">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/finding-target/status/reason" class="toc3 name">reason</h3>
                                 <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/finding-target/status/reason">Switch to XML</a></div>
                                 <p class="formal-name">Objective Status Reason</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> The reason the objective was given it's status.</p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>Reason may contain any value, and should be used to communicate additional information
                                             regarding the status.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <details>
                                    <summary>Constraint (1)</summary>
                                    
                                    <div class="constraint">
                                       <p><span class="usa-tag">allowed values</span></p>
                                       <p>The value <b>may be locally defined</b>, or one of the following:</p>
                                       <ul>
                                          
                                          <li><strong>pass</strong>: The target system or system component satisfied all the conditions.</li>
                                          
                                          <li><strong>fail</strong>: The target system or system component did not satisfy all the conditions.</li>
                                          
                                          <li><strong>other</strong>: Some other event took place that is not a pass or a fail. </li>
                                          </ul>
                                    </div>
                                    </details>
                              </div>
                           </div>
                           <div class="model-entry definition field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/finding-target/status/remarks" class="toc3 name">remarks</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/finding-target/status/remarks">Switch to XML</a></div>
                                 <p class="formal-name">Remarks</p>
                              </div>
                              <div class="body">
                                 <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/finding-target/implementation-status" class="toc2 name">implementation-status</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/finding-target/implementation-status">Switch to XML</a></div>
                     <p class="formal-name">Implementation Status</p>
                  </div>
                  <div class="body">
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>The <code>implementation-status</code> is used to qualify the <code>status</code> value to indicate the degree to which the control was found to be implemented.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-implementation-common/implementation-status">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/finding-target/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/finding-target/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-field">
      <div class="definition-header">
         <h1 id="/field/oscal-implementation-common/function-performed" class="toc1 name">function-performed</h1>
         <p class="type"><a href="/reference/datatypes/#string">string</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-implementation-common/function-performed">Switch to XML</a></div>
         <p class="formal-name">Functions Performed</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Describes a function performed for a given authorized privilege by this user class.</p>
      </div>
   </div>
   <div class="model-entry definition define-field">
      <div class="definition-header">
         <h1 id="/field/oscal-metadata/hash" class="toc1 name">hash</h1>
         <p class="type"><a href="/reference/datatypes/#string">string</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-metadata/hash">Switch to XML</a></div>
         <p class="formal-name">Hash</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A representation of a cryptographic digest generated over a resource using a specified
            hash algorithm.</p>
         <p><span class="usa-tag">value key</span> <code class="name">value</code></p>
         <div class="remarks-group usa-prose">
            <details open="open">
               <summary class="subhead">Remarks</summary>
               <div class="remarks">
                  <p>A hash value can be used to authenticate that a referenced resource is the same resources
                     as was pointed to by the author of the reference.</p>
               </div>
            </details>
         </div>
         <details open="open">
            <summary>Properties (2)</summary>
            <div class="model field-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/field/oscal-metadata/hash/algorithm" class="toc2 name">algorithm</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-metadata/hash/algorithm">Switch to XML</a></div>
                     <p class="formal-name">Hash algorithm</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Method by which a hash is derived</p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Any other value used MUST be a value defined in the W3C <a href="http://www.w3.org/TR/xmlsec-algorithms/#digest-method">XML Security Algorithm Cross-Reference</a> Digest Methods (W3C, April 2013) or <a href="https://tools.ietf.org/html/rfc6931#section-2.1.5">RFC 6931 Section 2.1.5</a> New SHA Functions.</p>
                           </div>
                        </details>
                     </div>
                     <details>
                        <summary>Constraint (1)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span></p>
                           <p>The value <b>may be locally defined</b>, or one of the following:</p>
                           <ul>
                              
                              <li><strong>SHA-224</strong>: The SHA-224 algorithm as defined by NIST FIPS 180-4.
                                 </li>
                              
                              <li><strong>SHA-256</strong>: The SHA-256 algorithm as defined by NIST FIPS 180-4.
                                 </li>
                              
                              <li><strong>SHA-384</strong>: The SHA-384 algorithm as defined by NIST FIPS 180-4.
                                 </li>
                              
                              <li><strong>SHA-512</strong>: The SHA-512 algorithm as defined by NIST FIPS 180-4.
                                 </li>
                              
                              <li><strong>SHA3-224</strong>: The SHA3-224 algorithm as defined by NIST FIPS 202.
                                 </li>
                              
                              <li><strong>SHA3-256</strong>: The SHA3-256 algorithm as defined by NIST FIPS 202.
                                 </li>
                              
                              <li><strong>SHA3-384</strong>: The SHA3-384 algorithm as defined by NIST FIPS 202.
                                 </li>
                              
                              <li><strong>SHA3-512</strong>: The SHA3-512 algorithm as defined by NIST FIPS 202.
                                 </li>
                              </ul>
                        </div>
                        </details>
                  </div>
               </div>
               <div class="model-entry definition m:define-flag">
                  <div class="instance-header">
                     <h2 id="/field/oscal-metadata/hash/value" class="toc2 name">value</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-metadata/hash">Switch to XML</a></div>
                     <p class="formal-name">Hash Value</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> This property provides the (nominal) value for this object as a whole.</p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-implementation-common/implementation-status" class="toc1 name">implementation-status</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/implementation-status">Switch to XML</a></div>
         <p class="formal-name">Implementation Status</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Indicates the degree to which the a given control is implemented.</p>
         <details open="open">
            <summary>Properties (2)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/implementation-status/state" class="toc2 name">state</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/implementation-status/state">Switch to XML</a></div>
                     <p class="formal-name">Implementation State</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Identifies the implementation status of the control or control objective.</p>
                     <details>
                        <summary>Constraint (1)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span></p>
                           <p>The value <b>may be locally defined</b>, or one of the following:</p>
                           <ul>
                              
                              <li><strong>implemented</strong>: The control is fully implemented.</li>
                              
                              <li><strong>partial</strong>: The control is partially implemented.</li>
                              
                              <li><strong>planned</strong>: There is a plan for implementing the control as explained in the remarks.</li>
                              
                              <li><strong>alternative</strong>: There is an alternative implementation for this control as explained in the remarks.</li>
                              
                              <li><strong>not-applicable</strong>: This control does not apply to this system as justified in the remarks.</li>
                              </ul>
                        </div>
                        </details>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/implementation-status/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/implementation-status/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-ar/import-ap" class="toc1 name">import-ap</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/import-ap">Switch to XML</a></div>
         <p class="formal-name">Import Assessment Plan</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Used by assessment-results to import information about the original plan for assessing
            the system.</p>
         <details open="open">
            <summary>Properties (2)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/import-ap/href" class="toc2 name">href</h2>
                     <p class="type"><a href="/reference/datatypes/#uri-reference">uri-reference</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/import-ap/href">Switch to XML</a></div>
                     <p class="formal-name">Assessment Plan Reference</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A resolvable URL reference to the assessment plan governing the assessment activities.</p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>The value of the <code>href</code> can be an internet resource, or a local reference using a fragment e.g. #fragment
                                 that points to a <code>back-matter</code> <code>resource</code> in the same document.</p>
                              <p>If a local reference using a fragment is used, this will be indicated by a fragment
                                 "#" followed by an identifier which references an identified <code>resource</code> in the document's <code>back-matter</code> or another object that is within the scope of the containing OSCAL document.</p>
                              <p>If an internet resource is used, the <code>href</code> value will be an absolute or relative URI pointing to the location of the referenced
                                 resource. A relative URI will be resolved relative to the location of the document
                                 containing the link.</p>
                           </div>
                        </details>
                     </div>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/import-ap/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/import-ap/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-assessment-common/import-ssp" class="toc1 name">import-ssp</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/import-ssp">Switch to XML</a></div>
         <p class="formal-name">Import System Security Plan</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Used by the assessment plan and POA&amp;M to import information about the system.</p>
         <details open="open">
            <summary>Properties (2)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/import-ssp/href" class="toc2 name">href</h2>
                     <p class="type"><a href="/reference/datatypes/#uri-reference">uri-reference</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/import-ssp/href">Switch to XML</a></div>
                     <p class="formal-name">System Security Plan Reference</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A resolvable URL reference to the system security plan for the system being assessed.</p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>The value of the <code>href</code> can be an internet resource, or a local reference using a fragment e.g. #fragment
                                 that points to a <code>back-matter</code> <code>resource</code> in the same document.</p>
                              <p>If a local reference using a fragment is used, this will be indicated by a fragment
                                 "#" followed by an identifier which references an identified <code>resource</code> in the document's <code>back-matter</code> or another object that is <a href="/concepts/layer/assessment/assessment-plan/#key-concepts">within the scope of the containing OSCAL document</a>.</p>
                              <p>If an internet resource is used, the <code>href</code> value will be an absolute or relative URI pointing to the location of the referenced
                                 resource. A relative URI will be resolved relative to the location of the document
                                 containing the link.</p>
                           </div>
                        </details>
                     </div>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/import-ssp/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/import-ssp/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-catalog-common/include-all" class="toc1 name">include-all</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/include-all">Switch to XML</a></div>
         <p class="formal-name">Include All</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Include all controls from the imported catalog or profile resources.</p>
         <div class="remarks-group usa-prose">
            <details open="open">
               <summary class="subhead">Remarks</summary>
               <div class="remarks">
                  <p>This element provides an alternative to calling controls individually from a catalog.</p>
               </div>
            </details>
         </div>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-implementation-common/inventory-item" class="toc1 name">inventory-item</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/inventory-item">Switch to XML</a></div>
         <p class="formal-name">Inventory Item</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A single managed inventory item within the system.</p>
         <details>
            <summary>Constraints (9)</summary>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">prop/@name</code></p>
               <p>The value <b>may be locally defined</b>, or one of the following:</p>
               <ul>
                  
                  <li><strong>ipv4-address</strong>: The Internet Protocol v4 Address of the asset.</li>
                  
                  <li><strong>ipv6-address</strong>: The Internet Protocol v6 Address of the asset.</li>
                  
                  <li><strong>fqdn</strong>: The full-qualified domain name (FQDN) of the asset.</li>
                  
                  <li><strong>uri</strong>: A Uniform Resource Identifier (URI) for the asset.</li>
                  
                  <li><strong>serial-number</strong>: A serial number for the asset.</li>
                  
                  <li><strong>netbios-name</strong>: The NetBIOS name for the asset.</li>
                  
                  <li><strong>mac-address</strong>: The media access control (MAC) address for the asset.</li>
                  
                  <li><strong>physical-location</strong>: The physical location of the asset's hardware (e.g., Data Center ID, Cage#, Rack#,
                     or other meaningful location identifiers).</li>
                  
                  <li><strong>is-scanned</strong>: is the asset subjected to network scans? (yes/no)</li>
                  
                  
                  
                  
                  
                  <li><strong>hardware-model</strong>: The model number of the hardware used by the asset.</li>
                  
                  
                  <li><strong>os-name</strong>: The name of the operating system used by the asset.</li>
                  
                  
                  <li><strong>os-version</strong>: The version of the operating system used by the asset.</li>
                  
                  
                  <li><strong>software-name</strong>: The software product name used by the asset.</li>
                  
                  
                  <li><strong>software-version</strong>: The software product version used by the asset.</li>
                  
                  
                  <li><strong>software-patch-level</strong>: The software product patch level used by the asset.</li>
                  
                  
                  
                  
                  
                  
                  <li><strong>asset-type</strong>: Simple indication of the asset's function, such as Router, Storage Array, DNS Server.</li>
                  
                  <li><strong>asset-id</strong>: An organizationally specific identifier that is used to uniquely identify a logical
                     or tangible item by the organization that owns the item.</li>
                  
                  <li><strong>asset-tag</strong>: An asset tag assigned by the organization responsible for maintaining the logical
                     or tangible item.</li>
                  
                  <li><strong>public</strong>: Identifies whether the asset is publicly accessible (yes/no)</li>
                  
                  <li><strong>virtual</strong>: Identifies whether the asset is virtualized (yes/no)</li>
                  
                  <li><strong>vlan-id</strong>: Virtual LAN identifier of the asset.</li>
                  
                  <li><strong>network-id</strong>: The network identifier of the asset.</li>
                  
                  <li><strong>label</strong>: A human-readable label for the parent context.</li>
                  
                  <li><strong>sort-id</strong>: An alternative identifier, whose value is easily sortable among other such values
                     in the document.</li>
                  
                  <li><strong>baseline-configuration-name</strong>: The name of the baseline configuration for the asset.</li>
                  
                  <li><strong>allows-authenticated-scan</strong>: Can the asset be check with an authenticated scan? (yes/no)</li>
                  
                  <li><strong>function</strong>: The function provided by the asset for the system.</li>
                  
                  
                  </ul>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">prop[@name='asset-type']/@value</code></p>
               <p>The value <b>must</b> be one of the following:</p>
               <ul>
                  
                  
                  
                  <li><strong>operating-system</strong>: System software that manages computer hardware, software resources, and provides
                     common services for computer programs.</li>
                  
                  <li><strong>database</strong>: An electronic collection of data, or information, that is specially organized for
                     rapid search and retrieval.</li>
                  
                  <li><strong>web-server</strong>: A system that delivers content or services to end users over the Internet or an
                     intranet.</li>
                  
                  <li><strong>dns-server</strong>: A system that resolves domain names to internet protocol (IP) addresses.</li>
                  
                  <li><strong>email-server</strong>: A computer system that sends and receives electronic mail messages.</li>
                  
                  <li><strong>directory-server</strong>: A  system that stores, organizes and provides access to directory information in
                     order to unify network resources.</li>
                  
                  <li><strong>pbx</strong>: A private branch exchange (PBX) provides a a private telephone switchboard.</li>
                  
                  <li><strong>firewall</strong>: A network security system that monitors and controls incoming and outgoing network
                     traffic based on predetermined security rules.</li>
                  
                  <li><strong>router</strong>: A physical or virtual networking device that forwards data packets between computer
                     networks.</li>
                  
                  <li><strong>switch</strong>: A physical or virtual networking device that connects devices within a computer
                     network by using packet switching to receive and forward data to the destination device.</li>
                  
                  <li><strong>storage-array</strong>: A consolidated, block-level data storage capability.</li>
                  
                  <li><strong>appliance</strong>: A physical or virtual machine that centralizes hardware, software, or services for
                     a specific purpose.</li>
                  
                  </ul>
            </div>
            
            
            <div class="constraint">
               <p><span class="usa-tag">allowed value</span> for <code class="path">(.)[@type=('software', 'hardware', 'service')]/prop/@name</code></p>
               <p>The value <b>may be locally defined</b>, or the following:</p>
               <ul>
                  
                  <li><strong>vendor-name</strong>: The name of the company or organization </li>
                  </ul>
            </div>
            
            
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">prop[@name='is-scanned']/@value</code></p>
               <p>The value <b>must</b> be one of the following:</p>
               <ul>
                  
                  <li><strong>yes</strong>: The asset is included in periodic vulnerability scanning.</li>
                  
                  <li><strong>no</strong>: The asset is not included in periodic vulnerability scanning.</li>
                  </ul>
            </div>
            
            
            <div class="constraint">
               <p><span class="usa-tag">allowed value</span> for <code class="path">link/@rel</code></p>
               <p>The value <b>may be locally defined</b>, or the following:</p>
               <ul>
                  
                  <li><strong>baseline-template</strong>: A reference to the baseline template used to configure the asset.</li>
                  </ul>
            </div>
            
            
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">responsible-party/@role-id</code></p>
               <p>The value <b>may be locally defined</b>, or one of the following:</p>
               <ul>
                  
                  <li><strong>asset-owner</strong>: Accountable for ensuring the asset is managed in accordance with organizational
                     policies and procedures.</li>
                  
                  <li><strong>asset-administrator</strong>: Responsible for administering a set of assets.</li>
                  
                  
                  <li><strong>security-operations</strong>: Members of the security operations center (SOC).</li>
                  
                  
                  <li><strong>network-operations</strong>: Members of the network operations center (NOC).</li>
                  
                  <li><strong>incident-response</strong>: Responsible for responding to an event that could lead to loss of, or disruption
                     to, an organization's operations, services or functions.</li>
                  
                  <li><strong>help-desk</strong>: Responsible for providing information and support to users.</li>
                  
                  
                  <li><strong>configuration-management</strong>: Responsible for the configuration management processes governing changes to the
                     asset.</li>
                  
                  
                  <li><strong>maintainer</strong>: Responsible for the creation and maintenance of a component.</li>
                  
                  <li><strong>provider</strong>: Organization responsible for providing the component, if this is different from
                     the "maintainer" (e.g., a reseller).</li>
                  
                  </ul>
            </div>
            
            
            <div class="constraint">
               <p><span class="usa-tag">index has key</span> for <code class="path">responsible-party</code>this value must correspond to a listing in the index <code>index-metadata-role-id</code> using a key constructed of key field(s) <code>@role-id</code></p>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">index has key</span> for <code class="path">responsible-party</code>this value must correspond to a listing in the index <code>index-metadata-party-uuid</code> using a key constructed of key field(s) <code>party-uuid</code></p>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">is unique</span> for <code class="path">responsible-party</code>: any target value must be unique (i.e., occur only once)</p>
            </div>
            </details>
         <details open="open">
            <summary>Properties (7)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/inventory-item/uuid" class="toc2 name">uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/inventory-item/uuid">Switch to XML</a></div>
                     <p class="formal-name">Inventory Item Universally Unique Identifier</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this inventory item elsewhere in <a href="/concepts/identifier-use/#scope">this or other OSCAL instances</a>. The locally defined <em>UUID</em> of the <code>inventory item</code> can be used to reference the data item locally or globally (e.g., in an imported
                        OSCAL instance). This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                        of the document.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/inventory-item/description" class="toc2 name">description</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/inventory-item/description">Switch to XML</a></div>
                     <p class="formal-name">Inventory Item Description</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A summary of the inventory item stating its purpose within the system.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/inventory-item/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/inventory-item/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/inventory-item/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/inventory-item/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/inventory-item/responsible-parties" class="toc2 name">responsible-party</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/inventory-item/responsible-party">Switch to XML</a></div>
                     <p class="formal-name">Responsible Party</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">responsible-parties</code></p>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/responsible-party">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/inventory-item/implemented-components" class="toc2 name">implemented-component</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/inventory-item/implemented-component">Switch to XML</a></div>
                     <p class="formal-name">Implemented Component</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> The set of components that are implemented in a given system inventory item.</p>
                     <p><span class="usa-tag">group as</span> <code class="name">implemented-components</code></p>
                     <details>
                        <summary>Constraints (4)</summary>
                        
                        
                        
                        
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">prop/@name</code></p>
                           <p>The value <b>may be locally defined</b>, or one of the following:</p>
                           <ul>
                              
                              
                              <li><strong>version</strong>: The version of the component.</li>
                              
                              <li><strong>patch-level</strong>: The specific patch level of the component.</li>
                              
                              <li><strong>model</strong>: The model of the component.</li>
                              
                              
                              <li><strong>release-date</strong>: The date the component was released, such as a software release date or policy publication
                                 date.</li>
                              
                              <li><strong>validation-type</strong>: Used with component-type='validation' to provide a well-known name for a kind of
                                 validation.</li>
                              
                              <li><strong>validation-reference</strong>: Used with component-type='validation' to indicate the validating body's assigned
                                 identifier for their validation of this component.</li>
                              
                              
                              
                              <li><strong>asset-type</strong>: Simple indication of the asset's function, such as Router, Storage Array, DNS Server.</li>
                              
                              <li><strong>asset-id</strong>: An organizationally specific identifier that is used to uniquely identify a logical
                                 or tangible item by the organization that owns the item.</li>
                              
                              <li><strong>asset-tag</strong>: An asset tag assigned by the organization responsible for maintaining the logical
                                 or tangible item.</li>
                              
                              <li><strong>public</strong>: Identifies whether the asset is publicly accessible (yes/no)</li>
                              
                              <li><strong>virtual</strong>: Identifies whether the asset is virtualized (yes/no)</li>
                              
                              <li><strong>vlan-id</strong>: Virtual LAN identifier of the asset.</li>
                              
                              <li><strong>network-id</strong>: The network identifier of the asset.</li>
                              
                              <li><strong>label</strong>: A human-readable label for the parent context.</li>
                              
                              <li><strong>sort-id</strong>: An alternative identifier, whose value is easily sortable among other such values
                                 in the document.</li>
                              
                              <li><strong>baseline-configuration-name</strong>: The name of the baseline configuration for the asset.</li>
                              
                              <li><strong>allows-authenticated-scan</strong>: Can the asset be check with an authenticated scan? (yes/no)</li>
                              
                              <li><strong>function</strong>: The function provided by the asset for the system.</li>
                              
                              
                              </ul>
                        </div>
                        
                        
                        <div class="constraint">
                           <p><span class="usa-tag">has cardinality</span> for <code class="path">prop[@name='asset-id']</code> the cardinality of  <code>prop[@name='asset-id']</code> is constrained: <b>1</b>; maximum <b>unbounded</b>.</p>
                        </div>
                        
                        
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span> for <code class="path">responsible-party/@role-id</code></p>
                           <p>The value <b>may be locally defined</b>, or one of the following:</p>
                           <ul>
                              
                              <li><strong>asset-owner</strong>: Accountable for ensuring the asset is managed in accordance with organizational
                                 policies and procedures.</li>
                              
                              <li><strong>asset-administrator</strong>: Responsible for administering a set of assets.</li>
                              
                              
                              <li><strong>security-operations</strong>: Members of the security operations center (SOC).</li>
                              
                              
                              <li><strong>network-operations</strong>: Members of the network operations center (NOC).</li>
                              
                              <li><strong>incident-response</strong>: Responsible for responding to an event that could lead to loss of, or disruption
                                 to, an organization's operations, services or functions.</li>
                              
                              <li><strong>help-desk</strong>: Responsible for providing information and support to users.</li>
                              
                              
                              <li><strong>configuration-management</strong>: Responsible for the configuration management processes governing changes to the
                                 asset.</li>
                              
                              </ul>
                        </div>
                        
                        
                        
                        
                        <div class="constraint">
                           <p><span class="usa-tag">is unique</span> for <code class="path">responsible-party</code>: any target value must be unique (i.e., occur only once)</p>
                        </div>
                        </details>
                     <details open="open">
                        <summary>Properties (5)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition define-flag">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-implementation-common/inventory-item/implemented-components/component-uuid" class="toc3 name">component-uuid</h3>
                                 <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/inventory-item/implemented-component/component-uuid">Switch to XML</a></div>
                                 <p class="formal-name">Component Universally Unique Identifier Reference</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a> identifier reference to a <code>component</code> that is implemented as part of an inventory item.</p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-implementation-common/inventory-item/implemented-components/props" class="toc3 name">property</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/inventory-item/implemented-component/prop">Switch to XML</a></div>
                                 <p class="formal-name">Property</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                                 <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>Properties permit the deployment and management of arbitrary controlled values, within
                                             OSCAL objects. A property can be included for any purpose useful to an application
                                             or implementation. Typically, properties will be used to sort, filter, select, order,
                                             and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                             an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                             lexical composition of properties may be constrained by external processes to ensure
                                             consistency.</p>
                                          <p>Property allows for associated remarks that describe why the specific property value
                                             was applied to the containing object, or the significance of the value in the context
                                             of the containing object.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-implementation-common/inventory-item/implemented-components/links" class="toc3 name">link</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/inventory-item/implemented-component/link">Switch to XML</a></div>
                                 <p class="formal-name">Link</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                             a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                                          <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-implementation-common/inventory-item/implemented-components/responsible-parties" class="toc3 name">responsible-party</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/inventory-item/implemented-component/responsible-party">Switch to XML</a></div>
                                 <p class="formal-name">Responsible Party</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">group as</span> <code class="name">responsible-parties</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>This construct is used to either: 1) associate a party or parties to a role defined
                                             on the component using the <code>responsible-role</code> construct, or 2) to define a party or parties that are responsible for a role defined
                                             within the context of the containing <code>inventory-item</code>. </p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/responsible-party">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-implementation-common/inventory-item/implemented-components/remarks" class="toc3 name">remarks</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/inventory-item/implemented-component/remarks">Switch to XML</a></div>
                                 <p class="formal-name">Remarks</p>
                              </div>
                              <div class="body">
                                 <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/inventory-item/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/inventory-item/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-field">
      <div class="definition-header">
         <h1 id="/field/oscal-metadata/last-modified" class="toc1 name">last-modified</h1>
         <p class="type"><a href="/reference/datatypes/#datetime-with-timezone">dateTime-with-timezone</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-metadata/last-modified">Switch to XML</a></div>
         <p class="formal-name">Last Modified Timestamp</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> The date and time the document was last modified. The date-time value must be formatted
            according to <a href="https://tools.ietf.org/html/rfc3339">RFC 3339</a> with full time and time zone included.</p>
         <div class="remarks-group usa-prose">
            <details open="open">
               <summary class="subhead">Remarks</summary>
               <div class="remarks">
                  <p>This value represents the point in time when the OSCAL document was last updated,
                     or at the point of creation the creation date. Typically, this date value will be
                     machine generated at time of creation or modification.</p>
                  <p>In some cases, an OSCAL document may be derived from some source material in a different
                     format. In such a case, the <code>last-modified</code> value should indicate the modification time of the OSCAL document, not the source
                     material.</p>
                  <p>A publisher of OSCAL content can use this data point along with its siblings <code>published</code> and <code>version</code> to establish a sequence of successive revisions of a given OSCAL-based publication.
                     The metadata for previous revisions can be represented as a <code>revision</code> in this object.</p>
               </div>
            </details>
         </div>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-metadata/link" class="toc1 name">link</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/link">Switch to XML</a></div>
         <p class="formal-name">Link</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A reference to a local or remote resource</p>
         <div class="remarks-group usa-prose">
            <details open="open">
               <summary class="subhead">Remarks</summary>
               <div class="remarks">
                  <p>To provide a cryptographic hash for a remote target resource, a local reference to
                     a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                  <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
               </div>
            </details>
         </div>
         <details>
            <summary>Constraints (3)</summary>
            
            <div class="constraint">
               <p><span class="usa-tag">matches</span> for <code class="path">.[@rel=('reference') and starts-with(@href,'#')]/@href</code>: the target value must match the lexical form of the 'uri-reference' data type.</p>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">index has key</span> for <code class="path">.[@rel=('reference') and starts-with(@href,'#')]</code>this value must correspond to a listing in the index <code>index-back-matter-resource</code> using a key constructed of key field(s) <code>@href</code></p>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">matches</span> for <code class="path">.[@rel=('reference') and not(starts-with(@href,'#'))]/@href</code>: the target value must match the lexical form of the 'uri' data type.</p>
            </div>
            </details>
         <details open="open">
            <summary>Properties (4)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/link/href" class="toc2 name">href</h2>
                     <p class="type"><a href="/reference/datatypes/#uri-reference">uri-reference</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/link/href">Switch to XML</a></div>
                     <p class="formal-name">Hypertext Reference</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A resolvable URL reference to a resource.</p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>The value of the <code>href</code> can be an internet resource, or a local reference using a fragment e.g. #fragment
                                 that points to a <code>back-matter</code> <code>resource</code> in the same document.</p>
                              <p>If a local reference using a fragment is used, this will be indicated by a fragment
                                 "#" followed by an identifier which references an identified <code>resource</code> in the document's <code>back-matter</code> or another object that is within the scope of the containing OSCAL document.</p>
                              <p>If an internet resource is used, the <code>href</code> value will be an absolute or relative URI pointing to the location of the referenced
                                 resource. A relative URI will be resolved relative to the location of the document
                                 containing the link.</p>
                           </div>
                        </details>
                     </div>
                  </div>
               </div>
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/link/rel" class="toc2 name">rel</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/link/rel">Switch to XML</a></div>
                     <p class="formal-name">Relation</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Describes the type of relationship provided by the link. This can be an indicator
                        of the link's purpose.</p>
                     <details>
                        <summary>Constraint (1)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed value</span></p>
                           <p>The value <b>may be locally defined</b>, or the following:</p>
                           <ul>
                              
                              <li><strong>reference</strong>: Reference</li>
                              </ul>
                        </div>
                        </details>
                  </div>
               </div>
               <div class="model-entry definition flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/link/media-type" class="toc2 name">media-type</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/link/media-type">Switch to XML</a></div>
                     <p class="formal-name">Media Type</p>
                  </div>
                  <div class="body">
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>The <code>media-type</code> provides a hint about the content model of the referenced resource. A valid entry
                                 from the <a href="https://www.iana.org/assignments/media-types/media-types.xhtml">IANA Media Types registry</a> SHOULD be used.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/flag/oscal-metadata/media-type">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/link/text" class="toc2 name">text</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/link/text">Switch to XML</a></div>
                     <p class="formal-name">Link Text</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A textual label to associate with the link, which may be used for presentation in
                        a tool.</p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-assessment-common/local-objective" class="toc1 name">local-objective</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/local-objective">Switch to XML</a></div>
         <p class="formal-name">Assessment-Specific Control Objective</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A local definition of a control objective for this assessment. Uses catalog syntax
            for control objective and assessment actions.</p>
         <details>
            <summary>Constraints (5)</summary>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">part[has-oscal-namespace('http://csrc.nist.gov/ns/oscal')]</code></p>
               <p>The value <b>must</b> be one of the following:</p>
               <ul>
                  
                  <li><strong>objective</strong>: **(deprecated)** Use 'assessment-objective' instead.</li>
                  
                  <li><strong>assessment</strong>: **(deprecated)** Use 'assessment-method' instead</li>
                  
                  <li><strong>assessment-objective</strong>: The part defines an assessment objective.</li>
                  
                  <li><strong>assessment-method</strong>: The part defines an assessment method.</li>
                  </ul>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">has cardinality</span> for <code class="path">part[has-oscal-namespace('http://csrc.nist.gov/ns/oscal') and @name=('objective','assessment-objective')]</code> the cardinality of  <code>part[has-oscal-namespace('http://csrc.nist.gov/ns/oscal') and @name=('objective','assessment-objective')]</code> is constrained: <b>0</b>; maximum <b>1</b>.</p>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">has cardinality</span> for <code class="path">part[has-oscal-namespace('http://csrc.nist.gov/ns/oscal') and @name=('assessment','assessment-method')]/prop[has-oscal-namespace(('http://csrc.nist.gov/ns/oscal','http://csrc.nist.gov/ns/rmf'))
                     and @name='method']</code> the cardinality of  <code>part[has-oscal-namespace('http://csrc.nist.gov/ns/oscal') and @name=('assessment','assessment-method')]/prop[has-oscal-namespace(('http://csrc.nist.gov/ns/oscal','http://csrc.nist.gov/ns/rmf'))
                     and @name='method']</code> is constrained: <b>1</b>; maximum <b>1</b>.</p>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">has cardinality</span> for <code class="path">part[has-oscal-namespace('http://csrc.nist.gov/ns/oscal') and @name=('assessment','assessment-method')]/part[has-oscal-namespace('http://csrc.nist.gov/ns/oscal')
                     and @name=('objects','assessment-objects')]</code> the cardinality of  <code>part[has-oscal-namespace('http://csrc.nist.gov/ns/oscal') and @name=('assessment','assessment-method')]/part[has-oscal-namespace('http://csrc.nist.gov/ns/oscal')
                     and @name=('objects','assessment-objects')]</code> is constrained: <b>1</b>; maximum <b>1</b>.</p>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">has cardinality</span> for <code class="path">part[has-oscal-namespace('http://csrc.nist.gov/ns/oscal') and @name=('objective','assessment-objective')]/prop[has-oscal-namespace('http://csrc.nist.gov/ns/oscal')
                     and @name='method-id']</code> the cardinality of  <code>part[has-oscal-namespace('http://csrc.nist.gov/ns/oscal') and @name=('objective','assessment-objective')]/prop[has-oscal-namespace('http://csrc.nist.gov/ns/oscal')
                     and @name='method-id']</code> is constrained: <b>1</b>; maximum <b>unbounded</b>.</p>
            </div>
            </details>
         <details open="open">
            <summary>Properties (6)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/local-objective/control-id" class="toc2 name">control-id</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/local-objective/control-id">Switch to XML</a></div>
                     <p class="formal-name">Control Identifier Reference</p>
                  </div>
                  <div class="body">
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>The specified <code>control-id</code> must be a valid value within the baseline identified by the target system's SSP via
                                 the <code>import-profile</code> statement.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/flag/oscal-catalog-common/control-id">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/local-objective/description" class="toc2 name">description</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/local-objective/description">Switch to XML</a></div>
                     <p class="formal-name">Objective Description</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A human-readable description of this control objective.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/local-objective/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/local-objective/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/local-objective/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/local-objective/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/local-objective/parts" class="toc2 name">part</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[1 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/local-objective/part">Switch to XML</a></div>
                     <p class="formal-name">Part</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">parts</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>A <code>part</code> provides for logical partitioning of prose, and can be thought of as a grouping structure
                                 (e.g., section). A <code>part</code> can have child parts allowing for arbitrary nesting of prose content (e.g., statement
                                 hierarchy). A <code>part</code> can contain <code>prop</code> objects that allow for enriching prose text with structured name/value information.</p>
                              <p>A <code>part</code> can be assigned an optional <code>id</code>, which allows for internal and external references to the textual concept contained
                                 within a <code>part</code>. A <code>id</code> provides a means for an OSCAL profile, or a higher layer OSCAL model to reference
                                 a specific part within a <code>catalog</code>. For example, an <code>id</code> can be used to reference or to make modifications to a control statement in a profile.</p>
                              <p>Use of <code>part</code> and <code>prop</code> provides for a wide degree of extensibility within the OSCAL catalog model. The optional
                                 <code>ns</code> provides a means to qualify a part's <code>name</code>, allowing for organization-specific vocabularies to be defined with clear semantics.
                                 Any organization that extends OSCAL in this way should consistently assign a <code>ns</code> value that represents the organization, making a given namespace qualified <code>name</code> unique to that organization. This allows the combination of <code>ns</code> and <code>name</code> to always be unique and unambiguous, even when mixed with extensions from other organizations.
                                 Each organization is responsible for governance of their own extensions, and is strongly
                                 encouraged to publish their extensions as standards to their user community. If no
                                 <code>ns</code> is provided, the name is expected to be in the "OSCAL" namespace.</p>
                              <p>To ensure a <code>ns</code> is unique to an organization and naming conflicts are avoided, a URI containing a
                                 DNS or other globally defined organization name should be used. For example, if FedRAMP
                                 and DoD both extend OSCAL, FedRAMP will use the <code>ns</code> "https://fedramp.gov", while DoD will use the <code>ns</code> "https://defense.gov" for any organization specific <code>name</code>. </p>
                              <p>Tools that process OSCAL content are not required to interpret unrecognized OSCAL
                                 extensions; however, OSCAL compliant tools should not modify or remove unrecognized
                                 extensions, unless there is a compelling reason to do so, such as data sensitivity.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-catalog-common/part">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/local-objective/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/local-objective/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-metadata/location" class="toc1 name">location</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/location">Switch to XML</a></div>
         <p class="formal-name">Location</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A location, with associated metadata that can be referenced.</p>
         <details>
            <summary>Constraints (3)</summary>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed value</span> for <code class="path">prop/@name</code></p>
               <p>The value <b>may be locally defined</b>, or the following:</p>
               <ul>
                  
                  <li><strong>type</strong>: Characterizes the kind of location.</li>
                  </ul>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed value</span> for <code class="path">prop[@name='type']/@value</code></p>
               <p>The value <b>may be locally defined</b>, or the following:</p>
               <ul>
                  
                  <li><strong>data-center</strong>: A location that contains computing assets. A class can be used to indicate the sub-type
                     of data-center as primary or alternate.</li>
                  </ul>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">prop[@name='type' and @value='data-center']/@class</code></p>
               <p>The value <b>may be locally defined</b>, or one of the following:</p>
               <ul>
                  
                  <li><strong>primary</strong>: The location is a data-center used for normal operations.</li>
                  
                  <li><strong>alternate</strong>: The location is a data-center used for fail-over or backup operations.</li>
                  </ul>
            </div>
            </details>
         <details open="open">
            <summary>Properties (9)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/location/uuid" class="toc2 name">uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/location/uuid">Switch to XML</a></div>
                     <p class="formal-name">Location Universally Unique Identifier</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this defined location elsewhere in <a href="/concepts/identifier-use/#scope">this or other OSCAL instances</a>. The locally defined <em>UUID</em> of the <code>location</code> can be used to reference the data item locally or globally (e.g., from an importing
                        OSCAL instance). This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                        of the document.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/location/title" class="toc2 name">title</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/location/title">Switch to XML</a></div>
                     <p class="formal-name">Location Title</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A name given to the location, which may be used by a tool for display and navigation.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/location/address" class="toc2 name">address</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/location/address">Switch to XML</a></div>
                     <p class="formal-name">Address</p>
                  </div>
                  <div class="body">
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Typically, the physical address of the location will be used here. If this information
                                 is sensitive, then a mailing address can be used instead.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/address">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/location/email-addresses" class="toc2 name">email-address</h2>
                     <p class="type"><a href="/reference/datatypes/#email">email</a></p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/location/email-address">Switch to XML</a></div>
                     <p class="formal-name">Email Address</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">email-addresses</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>This is a contact email associated with the location.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/field/oscal-metadata/email-address">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/location/telephone-numbers" class="toc2 name">telephone-number</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/location/telephone-number">Switch to XML</a></div>
                     <p class="formal-name">Telephone Number</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">telephone-numbers</code></p>
                     <p><span class="usa-tag">value key</span> <code class="name">number</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>A phone number used to contact the location.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/field/oscal-metadata/telephone-number">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/location/urls" class="toc2 name">url</h2>
                     <p class="type"><a href="/reference/datatypes/#uri">uri</a></p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/location/url">Switch to XML</a></div>
                     <p class="formal-name">Location URL</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> The uniform resource locator (URL) for a web site or Internet presence associated
                        with the location.</p>
                     <p><span class="usa-tag">group as</span> <code class="name">urls</code></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/location/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/location/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/location/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/location/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/location/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/location/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-flag">
      <div class="definition-header">
         <h1 id="/flag/oscal-metadata/location-type" class="toc1 name">location-type</h1>
         <p class="type"><a href="/reference/datatypes/#token">token</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/flag/oscal-metadata/location-type">Switch to XML</a></div>
         <p class="formal-name">Address Type</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Indicates the type of address.</p>
         <details>
            <summary>Constraint (1)</summary>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span></p>
               <p>The value <b>may be locally defined</b>, or one of the following:</p>
               <ul>
                  
                  <li><strong>home</strong>: A home address.</li>
                  
                  <li><strong>work</strong>: A work address.</li>
                  </ul>
            </div>
            </details>
      </div>
   </div>
   <div class="model-entry definition define-flag">
      <div class="definition-header">
         <h1 id="/flag/oscal-metadata/location-uuid" class="toc1 name">location-uuid</h1>
         <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/flag/oscal-metadata/location-uuid">Switch to XML</a></div>
         <p class="formal-name">Location Reference</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a> identifier reference to a <code>location</code> defined in the <code>metadata</code> section of this or another OSCAL instance. The <em>UUID</em> of the <code>location</code> in the source OSCAL instance is sufficient to reference the data item locally or
            globally (e.g., in an imported OSCAL instance). </p>
         <details>
            <summary>Constraint (1)</summary>
            
            
            <div class="constraint">
               <p><span class="usa-tag">index has key</span>this value must correspond to a listing in the index <code>index-metadata-location-uuid</code> using a key constructed of key field(s) <code>.</code></p>
            </div>
            </details>
      </div>
   </div>
   <div class="model-entry definition define-field">
      <div class="definition-header">
         <h1 id="/field/oscal-metadata/location-uuid" class="toc1 name">location-uuid</h1>
         <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-metadata/location-uuid">Switch to XML</a></div>
         <p class="formal-name">Location Reference</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a> identifier reference to a <code>location</code> defined in the <code>metadata</code> section of this or another OSCAL instance. The <em>UUID</em> of the <code>location</code> in the source OSCAL instance is sufficient to reference the data item locally or
            globally (e.g., in an imported OSCAL instance). </p>
         <div class="remarks-group usa-prose">
            <details open="open">
               <summary class="subhead">Remarks</summary>
               <div class="remarks">
                  <p>See the <a href="/concepts/identifier-use/#scope">Concepts - Identifier Use</a> page for additional information about the referenced identifier's scope.</p>
               </div>
            </details>
         </div>
         <details>
            <summary>Constraint (1)</summary>
            
            <div class="constraint">
               <p><span class="usa-tag">index has key</span>this value must correspond to a listing in the index <code>index-metadata-location-uuid</code> using a key constructed of key field(s) <code>.</code></p>
            </div>
            </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-assessment-common/logged-by" class="toc1 name">logged-by</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/logged-by">Switch to XML</a></div>
         <p class="formal-name">Logged By</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Used to indicate who created a log entry in what role.</p>
         <details open="open">
            <summary>Properties (2)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/logged-by/party-uuid" class="toc2 name">party-uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/logged-by/party-uuid">Switch to XML</a></div>
                     <p class="formal-name">Party UUID Reference</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a> identifier reference to the party who is making the log entry.</p>
                  </div>
               </div>
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/logged-by/role-id" class="toc2 name">role-id</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/logged-by/role-id">Switch to XML</a></div>
                     <p class="formal-name">Actor Role</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A point to the role-id of the role in which the party is making the log entry.</p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-flag">
      <div class="definition-header">
         <h1 id="/flag/oscal-metadata/media-type" class="toc1 name">media-type</h1>
         <p class="type"><a href="/reference/datatypes/#string">string</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/flag/oscal-metadata/media-type">Switch to XML</a></div>
         <p class="formal-name">Media Type</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Specifies a media type as defined by the Internet Assigned Numbers Authority (IANA)
            <a href="https://www.iana.org/assignments/media-types/media-types.xhtml">Media Types Registry</a>. </p>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-metadata/metadata" class="toc1 name">metadata</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/metadata">Switch to XML</a></div>
         <p class="formal-name">Publication metadata</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Provides information about the publication and availability of the containing document.</p>
         <details>
            <summary>Constraints (13)</summary>
            
            <div class="constraint">
               <p><span class="usa-tag">index</span> for <code class="path">role</code> an index <code>index-metadata-role-ids</code> shall list values returned by targets <code>role</code> using keys constructed of key field(s) <code>@id</code></p>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">is unique</span> for <code class="path">document-id</code>: any target value must be unique (i.e., occur only once)</p>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">is unique</span> for <code class="path">prop</code>: any target value must be unique (i.e., occur only once)</p>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">index</span> for <code class="path">.//prop</code> an index <code>index-metadata-property-uuid</code> shall list values returned by targets <code>.//prop</code> using keys constructed of key field(s) <code>@uuid</code></p>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">is unique</span> for <code class="path">link</code>: any target value must be unique (i.e., occur only once)</p>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">index</span> for <code class="path">role</code> an index <code>index-metadata-role-id</code> shall list values returned by targets <code>role</code> using keys constructed of key field(s) <code>@id</code></p>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">index</span> for <code class="path">location</code> an index <code>index-metadata-location-uuid</code> shall list values returned by targets <code>location</code> using keys constructed of key field(s) <code>@uuid</code></p>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">index</span> for <code class="path">party</code> an index <code>index-metadata-party-uuid</code> shall list values returned by targets <code>party</code> using keys constructed of key field(s) <code>@uuid</code></p>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">index</span> for <code class="path">party[@type='organization']</code> an index <code>index-metadata-party-organizations-uuid</code> shall list values returned by targets <code>party[@type='organization']</code> using keys constructed of key field(s) <code>@uuid</code></p>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">is unique</span> for <code class="path">responsible-party</code>: any target value must be unique (i.e., occur only once)</p>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">responsible-party/@role-id</code></p>
               <p>The value <b>may be locally defined</b>, or one of the following:</p>
               <ul>
                  
                  <li><strong>creator</strong>: Indicates the organization that created this content.</li>
                  
                  <li><strong>prepared-by</strong>: Indicates the organization that prepared this content.</li>
                  
                  <li><strong>prepared-for</strong>: Indicates the organization for which this content was created.</li>
                  
                  <li><strong>content-approver</strong>: Indicates the organization responsible for all content represented in the "document".</li>
                  
                  <li><strong>contact</strong>: Indicates the organization to contact for questions or support related to this content.</li>
                  </ul>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed value</span> for <code class="path">prop[has-oscal-namespace('http://csrc.nist.gov/ns/oscal')]/@name</code></p>
               <p>The value <b>must</b> be one of the following:</p>
               <ul>
                  
                  <li><strong>keywords</strong>: The value identifies a comma-seperated listing of keywords associated with this
                     content. These keywords may be used as search terms for indexing and other applications.</li>
                  </ul>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">link/@rel</code></p>
               <p>The value <b>may be locally defined</b>, or one of the following:</p>
               <ul>
                  
                  <li><strong>canonical</strong>: The link identifies the authoritative location for this file. Defined by RFC 6596.</li>
                  
                  <li><strong>alternate</strong>: The link identifies an alternative location or format for this file. Defined by
                     the HTML Living Standard</li>
                  
                  <li><strong>latest-version</strong>: This link identifies a resource containing the latest version in the version history.
                     Defined by RFC 5829.</li>
                  
                  <li><strong>predecessor-version</strong>: This link identifies a resource containing the predecessor version in the version
                     history. Defined by  RFC 5829.</li>
                  
                  <li><strong>successor-version</strong>: This link identifies a resource containing the predecessor version in the version
                     history. Defined by RFC 5829.</li>
                  </ul>
            </div>
            </details>
         <details open="open">
            <summary>Properties (14)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/metadata/title" class="toc2 name">title</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/metadata/title">Switch to XML</a></div>
                     <p class="formal-name">Document Title</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A name given to the document, which may be used by a tool for display and navigation.</p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/metadata/published" class="toc2 name">published</h2>
                     <p class="type"><a href="/reference/datatypes/#datetime-with-timezone">dateTime-with-timezone</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/metadata/published">Switch to XML</a></div>
                     <p class="formal-name">Publication Timestamp</p>
                  </div>
                  <div class="body">
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>This value represents the point in time when the OSCAL document was published. Typically,
                                 this date value will be machine generated at the time the containing document is published.</p>
                              <p>In some cases, an OSCAL document may be derived from some source material in a different
                                 format. In such a case, the <code>published</code> value should indicate when the OSCAL document was published, not the source material.
                                 Where necessary, the publication date of the original source material can be captured
                                 as a named property or custom metadata construct.</p>
                              <p>A publisher of OSCAL content can use this data point along with its siblings <code>last-modified</code> and <code>version</code> to establish a sequence of successive revisions of a given OSCAL-based publication.
                                 The metadata for previous revisions can be represented as a <code>revision</code> in this object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/field/oscal-metadata/published">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/metadata/last-modified" class="toc2 name">last-modified</h2>
                     <p class="type"><a href="/reference/datatypes/#datetime-with-timezone">dateTime-with-timezone</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/metadata/last-modified">Switch to XML</a></div>
                     <p class="formal-name">Last Modified Timestamp</p>
                  </div>
                  <div class="body">
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>This value represents the point in time when the OSCAL document was last updated,
                                 or at the point of creation the creation date. Typically, this date value will be
                                 machine generated at time of creation or modification.</p>
                              <p>In some cases, an OSCAL document may be derived from some source material in a different
                                 format. In such a case, the <code>last-modified</code> value should indicate the modification time of the OSCAL document, not the source
                                 material.</p>
                              <p>A publisher of OSCAL content can use this data point along with its siblings <code>published</code> and <code>version</code> to establish a sequence of successive revisions of a given OSCAL-based publication.
                                 The metadata for previous revisions can be represented as a <code>revision</code> in this object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/field/oscal-metadata/last-modified">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/metadata/version" class="toc2 name">version</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/metadata/version">Switch to XML</a></div>
                     <p class="formal-name">Document Version</p>
                  </div>
                  <div class="body">
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>A version string may be a release number, sequence number, date, or other identifier
                                 suffcient to distinguish between different document versions. This version is typically
                                 set by the document owner or by the tool used to maintain the content.</p>
                              <p>While not required, it is recommended that OSCAL content authors use <a href="https://semver.org/spec/v2.0.0.html">Semantic Versioning</a> as a format for version strings. This allows for the easy identification of a version
                                 tree consisting of major, minor, and patch numbers.</p>
                              <p>A publisher of OSCAL content can use this data point along with its siblings <code>published</code> and <code>last-modified</code> to establish a sequence of successive revisions of a given OSCAL-based publication.
                                 The metadata for previous revisions can be represented as a <code>revision</code> in this object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/field/oscal-metadata/version">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/metadata/oscal-version" class="toc2 name">oscal-version</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/metadata/oscal-version">Switch to XML</a></div>
                     <p class="formal-name">OSCAL version</p>
                  </div>
                  <div class="body">
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Indicates the version of the OSCAL model to which this data set conforms, for example
                                 <q>1.1.0</q> or <q>1.0.0-M1</q>. That can be used as a hint by a tool to indicate which version of the OSCAL XML
                                 or JSON schema to use for validation.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/field/oscal-metadata/oscal-version">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/metadata/revisions" class="toc2 name">revision</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/metadata/revisions/revision">Switch to XML</a></div>
                     <p class="formal-name">Revision History Entry</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">revisions</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>While <code>published</code>, <code>last-modified</code>, <code>oscal-version</code>, and <code>version</code> are not required, values for these entries should be provided if the information
                                 is known. For a revision entry to be considered valid, at least one of the following
                                 items must be provided: <code>published</code>, <code>last-modified</code>, <code>version</code>, or a <code>link</code> with a <code>rel</code> of <q>source</q>.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/revision">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/metadata/document-ids" class="toc2 name">document-id</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/metadata/document-id">Switch to XML</a></div>
                     <p class="formal-name">Document Identifier</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">document-ids</code></p>
                     <p><span class="usa-tag">value key</span> <code class="name">identifier</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>This element is optional, but it will always have a valid value, as if it is missing
                                 the value of "document-id" is assumed to be equal to the UUID of the root. This requirement
                                 allows for document creators to retroactively link an update to the original version,
                                 by providing a document-id on the new document that is equal to the uuid of the original
                                 document.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/field/oscal-metadata/document-id">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/metadata/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/metadata/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/metadata/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/metadata/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/metadata/roles" class="toc2 name">role</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/metadata/role">Switch to XML</a></div>
                     <p class="formal-name">Role</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">roles</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Permissible values to be determined closer to the application (e.g. by a receiving
                                 authority).</p>
                              <p>OSCAL has defined a set of standardized roles for consistent use in OSCAL documents.
                                 This allows tools consuming OSCAL content to infer specific semantics when these roles
                                 are used. These roles are documented in the specific contexts of their use (e.g.,
                                 responsible-party, responsible-role). When using such a role, it is necessary to define
                                 these roles in this list, which will then allow such a role to be referenced.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/role">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/metadata/locations" class="toc2 name">location</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/metadata/location">Switch to XML</a></div>
                     <p class="formal-name">Location</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">locations</code></p>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/location">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/metadata/parties" class="toc2 name">party</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/metadata/party">Switch to XML</a></div>
                     <p class="formal-name">Party (organization or person)</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">parties</code></p>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/party">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/metadata/responsible-parties" class="toc2 name">responsible-party</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/metadata/responsible-party">Switch to XML</a></div>
                     <p class="formal-name">Responsible Party</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">responsible-parties</code></p>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/responsible-party">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/metadata/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/metadata/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-flag">
      <div class="definition-header">
         <h1 id="/flag/oscal-assessment-common/objective-id" class="toc1 name">objective-id</h1>
         <p class="type"><a href="/reference/datatypes/#token">token</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/flag/oscal-assessment-common/objective-id">Switch to XML</a></div>
         <p class="formal-name">Objective ID</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Points to an assessment objective.</p>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-assessment-common/observation" class="toc1 name">observation</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/observation">Switch to XML</a></div>
         <p class="formal-name">Observation</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Describes an individual observation.</p>
         <details open="open">
            <summary>Properties (13)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/observation/uuid" class="toc2 name">uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/observation/uuid">Switch to XML</a></div>
                     <p class="formal-name">Observation Universally Unique Identifier</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <em>cross-instance</em> scope that can be used to reference this observation elsewhere in <a href="/concepts/identifier-use/#scope">this or other OSCAL instances</a>. The locally defined <em>UUID</em> of the <code>observation</code> can be used to reference the data item locally or globally (e.g., in an imorted OSCAL
                        instance). This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                        of the document.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/observation/title" class="toc2 name">title</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/observation/title">Switch to XML</a></div>
                     <p class="formal-name">Observation Title</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> The title for this observation.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/observation/description" class="toc2 name">description</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/observation/description">Switch to XML</a></div>
                     <p class="formal-name">Observation Description</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A human-readable description of this assessment observation.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/observation/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/observation/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/observation/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/observation/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/observation/methods" class="toc2 name">method</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[1 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/observation/method">Switch to XML</a></div>
                     <p class="formal-name">Observation Method</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Identifies how the observation was made.</p>
                     <p><span class="usa-tag">group as</span> <code class="name">methods</code></p>
                     <details>
                        <summary>Constraint (1)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span></p>
                           <p>The value <b>may be locally defined</b>, or one of the following:</p>
                           <ul>
                              
                              <li><strong>EXAMINE</strong>: An inspection was performed.</li>
                              
                              <li><strong>INTERVIEW</strong>: An interview was performed.</li>
                              
                              <li><strong>TEST</strong>: A manual or automated test was performed.</li>
                              
                              <li><strong>UNKNOWN</strong>: This is only for use when converting historic content to OSCAL, where the conversion
                                 process cannot initially identify the appropriate method(s).</li>
                              </ul>
                        </div>
                        </details>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/observation/types" class="toc2 name">type</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/observation/type">Switch to XML</a></div>
                     <p class="formal-name">Observation Type</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Identifies the nature of the observation. More than one may be used to further qualify
                        and enable filtering.</p>
                     <p><span class="usa-tag">group as</span> <code class="name">types</code></p>
                     <details>
                        <summary>Constraint (1)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span></p>
                           <p>The value <b>may be locally defined</b>, or one of the following:</p>
                           <ul>
                              
                              <li><strong>ssp-statement-issue</strong>: A difference between the SSP implementation statement, and actual implementation.</li>
                              
                              <li><strong>control-objective</strong>: An observation about the status of a the associated control objective.</li>
                              
                              <li><strong>mitigation</strong>: A mitigating factor was identified.</li>
                              
                              <li><strong>finding</strong>: An assessment finding. Used for observations made by tools, penetration testing,
                                 and other means.</li>
                              
                              <li><strong>historic</strong>: An observation from a past assessment, which was converted to OSCAL at a later date.</li>
                              </ul>
                        </div>
                        </details>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/observation/origins" class="toc2 name">origin</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/observation/origin">Switch to XML</a></div>
                     <p class="formal-name">Origin</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">origins</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Used to identify the individual and/or tool that gathered the evidence resulting in
                                 the observation identification.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-assessment-common/origin">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/observation/subjects" class="toc2 name">subject</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/observation/subject">Switch to XML</a></div>
                     <p class="formal-name">Identifies the Subject</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">subject</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">subjects</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>The subject reference UUID could point to an item defined in the SSP, AP, or AR.</p>
                              <p>Tools should check look for the ID in every file imported directly or indirectly.</p>
                           </div>
                           <div class="remarks">
                              <p>Identifies who was interviewed, or what was tested or inspected.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-assessment-common/subject-reference">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/observation/relevant-evidence" class="toc2 name">relevant-evidence</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/observation/relevant-evidence">Switch to XML</a></div>
                     <p class="formal-name">Relevant Evidence</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Links this observation to relevant evidence.</p>
                     <p><span class="usa-tag">group as</span> <code class="name">relevant-evidence</code></p>
                     <details open="open">
                        <summary>Properties (5)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition define-flag">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/observation/relevant-evidence/href" class="toc3 name">href</h3>
                                 <p class="type"><a href="/reference/datatypes/#uri-reference">uri-reference</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/observation/relevant-evidence/href">Switch to XML</a></div>
                                 <p class="formal-name">Relevant Evidence Reference</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A resolvable URL reference to relevant evidence.</p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>The value of the <code>href</code> can be an internet resource, or a local reference using a fragment e.g. #fragment
                                             that points to a <code>back-matter</code> <code>resource</code> in the same document.</p>
                                          <p>If a local reference using a fragment is used, this will be indicated by a fragment
                                             "#" followed by an identifier which references an identified <code>resource</code> in the document's <code>back-matter</code> or another object that is <a href="/concepts/layer/assessment/assessment-plan/#key-concepts">within the scope of the containing OSCAL document</a>.</p>
                                          <p>If an internet resource is used, the <code>href</code> value will be an absolute or relative URI pointing to the location of the referenced
                                             resource. A relative URI will be resolved relative to the location of the document
                                             containing the link.</p>
                                       </div>
                                    </details>
                                 </div>
                              </div>
                           </div>
                           <div class="model-entry definition define-field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/observation/relevant-evidence/description" class="toc3 name">description</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                 <p class="occurrence">[1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/observation/relevant-evidence/description">Switch to XML</a></div>
                                 <p class="formal-name">Relevant Evidence Description</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A human-readable description of this evidence.</p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/observation/relevant-evidence/props" class="toc3 name">property</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/observation/relevant-evidence/prop">Switch to XML</a></div>
                                 <p class="formal-name">Property</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                                 <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>Properties permit the deployment and management of arbitrary controlled values, within
                                             OSCAL objects. A property can be included for any purpose useful to an application
                                             or implementation. Typically, properties will be used to sort, filter, select, order,
                                             and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                             an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                             lexical composition of properties may be constrained by external processes to ensure
                                             consistency.</p>
                                          <p>Property allows for associated remarks that describe why the specific property value
                                             was applied to the containing object, or the significance of the value in the context
                                             of the containing object.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/observation/relevant-evidence/links" class="toc3 name">link</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/observation/relevant-evidence/link">Switch to XML</a></div>
                                 <p class="formal-name">Link</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                             a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                                          <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/observation/relevant-evidence/remarks" class="toc3 name">remarks</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/observation/relevant-evidence/remarks">Switch to XML</a></div>
                                 <p class="formal-name">Remarks</p>
                              </div>
                              <div class="body">
                                 <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/observation/collected" class="toc2 name">collected</h2>
                     <p class="type"><a href="/reference/datatypes/#datetime-with-timezone">dateTime-with-timezone</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/observation/collected">Switch to XML</a></div>
                     <p class="formal-name">collected field</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Date/time stamp identifying when the finding information was collected.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/observation/expires" class="toc2 name">expires</h2>
                     <p class="type"><a href="/reference/datatypes/#datetime-with-timezone">dateTime-with-timezone</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/observation/expires">Switch to XML</a></div>
                     <p class="formal-name">expires field</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Date/time identifying when the finding information is out-of-date and no longer valid.
                        Typically used with continuous assessment scenarios.</p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/observation/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/observation/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-assessment-common/origin" class="toc1 name">origin</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/origin">Switch to XML</a></div>
         <p class="formal-name">Origin</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Identifies the source of the finding, such as a tool, interviewed person, or activity.</p>
         <details open="open">
            <summary>Properties (2)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/origin/actors" class="toc2 name">actor</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[1 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/origin/actor">Switch to XML</a></div>
                     <p class="formal-name">Originating Actor</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">actor</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">actors</code></p>
                     <p class="definition-link"><a href="#/assembly/oscal-assessment-common/origin-actor">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/origin/related-tasks" class="toc2 name">related-task</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/origin/related-task">Switch to XML</a></div>
                     <p class="formal-name">Task Reference</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">related-tasks</code></p>
                     <p class="definition-link"><a href="#/assembly/oscal-assessment-common/related-task">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-assessment-common/origin-actor" class="toc1 name">origin-actor</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/origin-actor">Switch to XML</a></div>
         <p class="formal-name">Originating Actor</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> The actor that produces an observation, a finding, or a risk. One or more actor type
            can be used to specify a person that is using a tool.</p>
         <details open="open">
            <summary>Properties (5)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/origin-actor/type" class="toc2 name">type</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/origin-actor/type">Switch to XML</a></div>
                     <p class="formal-name">Actor Type</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> The kind of actor.</p>
                     <details>
                        <summary>Constraint (1)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>tool</strong>: A reference to a tool component defined with the assessment assets.</li>
                              
                              <li><strong>assessment-platform</strong>: A reference to an assessment-platform defined with the assessment assets.</li>
                              
                              <li><strong>party</strong>: A reference to a party defined within the document metadata.</li>
                              </ul>
                        </div>
                        </details>
                  </div>
               </div>
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/origin-actor/actor-uuid" class="toc2 name">actor-uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/origin-actor/actor-uuid">Switch to XML</a></div>
                     <p class="formal-name">Actor Universally Unique Identifier Reference</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a> identifier reference to the tool or person based on the associated type.</p>
                  </div>
               </div>
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/origin-actor/role-id" class="toc2 name">role-id</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/origin-actor/role-id">Switch to XML</a></div>
                     <p class="formal-name">Actor Role</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> For a party, this can optionally be used to specify the role the actor was performing.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/origin-actor/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/origin-actor/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/origin-actor/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/origin-actor/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-field">
      <div class="definition-header">
         <h1 id="/field/oscal-metadata/oscal-version" class="toc1 name">oscal-version</h1>
         <p class="type"><a href="/reference/datatypes/#string">string</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-metadata/oscal-version">Switch to XML</a></div>
         <p class="formal-name">OSCAL version</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> The OSCAL model version the document was authored against.</p>
         <div class="remarks-group usa-prose">
            <details open="open">
               <summary class="subhead">Remarks</summary>
               <div class="remarks">
                  <p>Indicates the version of the OSCAL model to which this data set conforms, for example
                     <q>1.1.0</q> or <q>1.0.0-M1</q>. That can be used as a hint by a tool to indicate which version of the OSCAL XML
                     or JSON schema to use for validation.</p>
               </div>
            </details>
         </div>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-catalog-common/parameter" class="toc1 name">param</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/parameter">Switch to XML</a></div>
         <p class="formal-name">Parameter</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Parameters provide a mechanism for the dynamic assignment of value(s) in a control.</p>
         <p><span class="usa-tag">use name</span> <code class="name">param</code></p>
         <div class="remarks-group usa-prose">
            <details open="open">
               <summary class="subhead">Remarks</summary>
               <div class="remarks">
                  <p>In a catalog, a parameter is typically used as a placeholder for the future assignment
                     of a parameter value, although the OSCAL model allows for the direct assignment of
                     a value if desired by the control author. The <code>value</code> may be optionally used to specify one or more values. If no value is provided, then
                     it is expected that the value will be provided at the Profile or Implementation layer.</p>
                  <p>A parameter can include a variety of metadata options that support the future solicitation
                     of one or more values. A <code>label</code> provides a textual placeholder that can be used in a tool to solicit parameter value
                     input, or to display in catalog documentation. The <code>desc</code> provides a short description of what the parameter is used for, which can be used
                     in tooling to help a user understand how to use the parameter. A <code>constraint</code> can be used to provide criteria for the allowed values. A <code>guideline</code> provides a recommendation for the use of a parameter.</p>
               </div>
            </details>
         </div>
         <details>
            <summary>Constraints (2)</summary>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">prop[has-oscal-namespace('http://csrc.nist.gov/ns/oscal')]/@name</code></p>
               <p>The value <b>must</b> be one of the following:</p>
               <ul>
                  
                  <li><strong>label</strong>: A human-readable label for the parent context, which may be rendered in place of
                     the actual identifier for some use cases.</li>
                  
                  <li><strong>sort-id</strong>: An alternative identifier, whose value is easily sortable among other such values
                     in the document.</li>
                  
                  <li><strong>alt-identifier</strong>: An alternate or aliased identifier for the parent context.</li>
                  
                  
                  <li><strong>alt-label</strong>: An alternate to the value provided by the parameter's label. This will typically
                     be qualified by a class.</li>
                  </ul>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed value</span> for <code class="path">prop[has-oscal-namespace('http://csrc.nist.gov/ns/rmf')]/@name</code></p>
               <p>The value <b>must</b> be one of the following:</p>
               <ul>
                  
                  <li><strong>aggregates</strong>: The parent parameter provides an aggregation of 2 or more other parameters, each
                     described by this property.</li>
                  </ul>
            </div>
            
            depends-on is deprecated
            
            </details>
         <details open="open">
            <summary>Properties (11)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/parameter/id" class="toc2 name">id</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/parameter/id">Switch to XML</a></div>
                     <p class="formal-name">Parameter Identifier</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#human-oriented">human-oriented</a>, <a href="/concepts/identifier-use/#locally-unique">locally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this defined parameter elsewhere in <a href="/concepts/identifier-use/#scope">this or other OSCAL instances</a>. When referenced from another OSCAL instance, this identifier must be referenced
                        in the context of the containing resource (e.g., import-profile). This id should be
                        assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                        of the document.</p>
                  </div>
               </div>
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/parameter/class" class="toc2 name">class</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/parameter/class">Switch to XML</a></div>
                     <p class="formal-name">Parameter Class</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A textual label that provides a characterization of the parameter.</p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>A <code>class</code> can be used in validation rules to express extra constraints over named items of
                                 a specific <code>class</code> value.</p>
                           </div>
                        </details>
                     </div>
                  </div>
               </div>
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/parameter/depends-on" class="toc2 name">depends-on</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/parameter/depends-on">Switch to XML</a></div>
                     <p class="formal-name">Depends on</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> **(deprecated)** Another parameter invoking this one. This construct has been deprecated
                        and should not be used.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/parameter/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/parameter/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/parameter/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/parameter/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/parameter/label" class="toc2 name">label</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/parameter/label">Switch to XML</a></div>
                     <p class="formal-name">Parameter Label</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A short, placeholder name for the parameter, which can be used as a substitute for
                        a <code>value</code> if no value is assigned.</p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>The label value should be suitable for inline display in a rendered catalog.</p>
                           </div>
                        </details>
                     </div>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/parameter/usage" class="toc2 name">usage</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/parameter/usage">Switch to XML</a></div>
                     <p class="formal-name">Parameter Usage Description</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Describes the purpose and use of a parameter</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/parameter/constraints" class="toc2 name">constraint</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/parameter/constraint">Switch to XML</a></div>
                     <p class="formal-name">Constraint</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">constraint</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">constraints</code></p>
                     <p class="definition-link"><a href="#/assembly/oscal-catalog-common/parameter-constraint">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/parameter/guidelines" class="toc2 name">guideline</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/parameter/guideline">Switch to XML</a></div>
                     <p class="formal-name">Guideline</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">guideline</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">guidelines</code></p>
                     <p class="definition-link"><a href="#/assembly/oscal-catalog-common/parameter-guideline">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/parameter/values" class="toc2 name">value</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/parameter/value">Switch to XML</a></div>
                     <p class="formal-name">Parameter Value</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">value</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">values</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>A set of values provided in a catalog can be redefined at any higher layer of OSCAL
                                 (e.g., Profile).</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/field/oscal-catalog-common/parameter-value">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/parameter/select" class="toc2 name">select</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/parameter/select">Switch to XML</a></div>
                     <p class="formal-name">Selection</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">select</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>A set of parameter value choices, that may be picked from to set the parameter value.</p>
                           </div>
                           <div class="remarks">
                              <p>A set of parameter value choices, that may be picked from to set the parameter value.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-catalog-common/parameter-selection">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/parameter/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/parameter/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-flag">
      <div class="definition-header">
         <h1 id="/flag/oscal-implementation-common/param-id" class="toc1 name">param-id</h1>
         <p class="type"><a href="/reference/datatypes/#token">token</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/flag/oscal-implementation-common/param-id">Switch to XML</a></div>
         <p class="formal-name">Parameter ID</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#human-oriented">human-oriented</a> reference to a <code>parameter</code> within a control, who's catalog has been imported into the current implementation
            context.</p>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-catalog-common/parameter-constraint" class="toc1 name">parameter-constraint</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/parameter-constraint">Switch to XML</a></div>
         <p class="formal-name">Constraint</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A formal or informal expression of a constraint or test</p>
         <details open="open">
            <summary>Properties (2)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/parameter-constraint/description" class="toc2 name">description</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/parameter-constraint/description">Switch to XML</a></div>
                     <p class="formal-name">Constraint Description</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A textual summary of the constraint to be applied.</p>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/parameter-constraint/tests" class="toc2 name">test</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/parameter-constraint/test">Switch to XML</a></div>
                     <p class="formal-name">Constraint Test</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A test expression which is expected to be evaluated by a tool.</p>
                     <p><span class="usa-tag">group as</span> <code class="name">tests</code></p>
                     <details open="open">
                        <summary>Properties (2)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition define-field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-catalog-common/parameter-constraint/tests/expression" class="toc3 name">expression</h3>
                                 <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                                 <p class="occurrence">[1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/parameter-constraint/test/expression">Switch to XML</a></div>
                                 <p class="formal-name">Constraint test</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A formal (executable) expression of a constraint</p>
                              </div>
                           </div>
                           <div class="model-entry definition field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-catalog-common/parameter-constraint/tests/remarks" class="toc3 name">remarks</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/parameter-constraint/test/remarks">Switch to XML</a></div>
                                 <p class="formal-name">Remarks</p>
                              </div>
                              <div class="body">
                                 <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-catalog-common/parameter-guideline" class="toc1 name">parameter-guideline</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/parameter-guideline">Switch to XML</a></div>
         <p class="formal-name">Guideline</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A prose statement that provides a recommendation for the use of a parameter.</p>
         <details open="open">
            <summary>Property (1)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/parameter-guideline/prose" class="toc2 name">prose</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/parameter-guideline/prose">Switch to XML</a></div>
                     <p class="formal-name">Guideline Text</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Prose permits multiple paragraphs, lists, tables etc.</p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-catalog-common/parameter-selection" class="toc1 name">parameter-selection</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/parameter-selection">Switch to XML</a></div>
         <p class="formal-name">Selection</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Presenting a choice among alternatives</p>
         <div class="remarks-group usa-prose">
            <details open="open">
               <summary class="subhead">Remarks</summary>
               <div class="remarks">
                  <p>A set of parameter value choices, that may be picked from to set the parameter value.</p>
               </div>
            </details>
         </div>
         <details open="open">
            <summary>Properties (2)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/parameter-selection/how-many" class="toc2 name">how-many</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/parameter-selection/how-many">Switch to XML</a></div>
                     <p class="formal-name">Parameter Cardinality</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Describes the number of selections that must occur. Without this setting, only one
                        value should be assumed to be permitted.</p>
                     <details>
                        <summary>Constraint (1)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>one</strong>: Only one value is permitted.</li>
                              
                              <li><strong>one-or-more</strong>: One or more values are permitted.</li>
                              </ul>
                        </div>
                        </details>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/parameter-selection/choice" class="toc2 name">choice</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/parameter-selection/choice">Switch to XML</a></div>
                     <p class="formal-name">Choice</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A value selection among several such options</p>
                     <p><span class="usa-tag">use name</span> <code class="name">choice</code></p>
                     <p><span class="usa-tag">value key</span> <code class="name">value</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">choice</code></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-field">
      <div class="definition-header">
         <h1 id="/field/oscal-catalog-common/parameter-value" class="toc1 name">parameter-value</h1>
         <p class="type"><a href="/reference/datatypes/#string">string</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-catalog-common/parameter-value">Switch to XML</a></div>
         <p class="formal-name">Parameter Value</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A parameter value or set of values.</p>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-assessment-common/assessment-part" class="toc1 name">part</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-part">Switch to XML</a></div>
         <p class="formal-name">Assessment Part</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A partition of an assessment plan or results or a child of another part.</p>
         <p><span class="usa-tag">use name</span> <code class="name">part</code></p>
         <div class="remarks-group usa-prose">
            <details open="open">
               <summary class="subhead">Remarks</summary>
               <div class="remarks">
                  <p>A <code>part</code> provides for logical partitioning of prose, and can be thought of as a grouping structure
                     (e.g., section). A <code>part</code> can have child parts allowing for arbitrary nesting of prose content (e.g., statement
                     hierarchy). A <code>part</code> can contain <code>prop</code> objects that allow for enriching prose text with structured name/value information.</p>
                  <p>A <code>part</code> can be assigned an optional <code>id</code>, which allows for internal and external references to the textual concept contained
                     within a <code>part</code>. A <code>id</code> provides a means for an OSCAL profile, or a higher layer OSCAL model to reference
                     a specific part within a <code>catalog</code>. For example, an <code>id</code> can be used to reference or to make modifications to a control statement in a profile.</p>
                  <p>Use of <code>part</code> and <code>prop</code> provides for a wide degree of extensibility within the OSCAL catalog model. The optional
                     <code>ns</code> provides a means to qualify a part's <code>name</code>, allowing for organization-specific vocabularies to be defined with clear semantics.
                     Any organization that extends OSCAL in this way should consistently assign a <code>ns</code> value that represents the organization, making a given namespace qualified <code>name</code> unique to that organization. This allows the combination of <code>ns</code> and <code>name</code> to always be unique and unambiguous, even when mixed with extensions from other organizations.
                     Each organization is responsible for governance of their own extensions, and is strongly
                     encouraged to publish their extensions as standards to their user community. If no
                     <code>ns</code> is provided, the name is expected to be in the "OSCAL" namespace.</p>
                  <p>To ensure a <code>ns</code> is unique to an organization and naming conflicts are avoided, a URI containing a
                     DNS or other globally defined organization name should be used. For example, if FedRAMP
                     and DoD both extend OSCAL, FedRAMP will use the <code>ns</code> "https://fedramp.gov", while DoD will use the <code>ns</code> "https://defense.gov" for any organization specific <code>name</code>.</p>
                  <p>Tools that process OSCAL content are not required to interpret unrecognized OSCAL
                     extensions; however, OSCAL compliant tools should not modify or remove unrecognized
                     extensions, unless there is a compelling reason to do so, such as data sensitivity.</p>
               </div>
            </details>
         </div>
         <details>
            <summary>Constraints (3)</summary>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed value</span> for <code class="path">.[@name='objective']/prop/@name</code></p>
               <p>The value <b>may be locally defined</b>, or the following:</p>
               <ul>
                  
                  <li><strong>method</strong>: The assessment method to use. This typically appears on parts with the name "objective".</li>
                  </ul>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">has cardinality</span> for <code class="path">.[@name='objective']/prop[@name='method']</code> the cardinality of  <code>.[@name='objective']/prop[@name='method']</code> is constrained: <b>1</b>; maximum <b>unbounded</b>.</p>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">.[@name='objective']/prop[@name='method']/@value</code></p>
               <p>The value <b>must</b> be one of the following:</p>
               <ul>
                  
                  <li><strong>INTERVIEW</strong>: The process of holding discussions with individuals or groups of individuals within
                     an organization to once again, facilitate assessor understanding, achieve clarification,
                     or obtain evidence.</li>
                  
                  <li><strong>EXAMINE</strong>: The process of reviewing, inspecting, observing, studying, or analyzing one or more
                     assessment objects (i.e., specifications, mechanisms, or activities).</li>
                  
                  <li><strong>TEST</strong>: The process of exercising one or more assessment objects (i.e., activities or mechanisms)
                     under specified conditions to compare actual with expected behavior.</li>
                  </ul>
            </div>
            </details>
         <details open="open">
            <summary>Properties (9)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-part/uuid" class="toc2 name">uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-part/uuid">Switch to XML</a></div>
                     <p class="formal-name">Part Identifier</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this part elsewhere in <a href="/concepts/identifier-use/#scope">this or other OSCAL instances</a>. The locally defined <em>UUID</em> of the <code>part</code> can be used to reference the data item locally or globally (e.g., in an ported OSCAL
                        instance). This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                        of the document.</p>
                  </div>
               </div>
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-part/name" class="toc2 name">name</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-part/name">Switch to XML</a></div>
                     <p class="formal-name">Part Name</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A textual label that uniquely identifies the part's semantic type.</p>
                     <details>
                        <summary>Constraint (1)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span></p>
                           <p>The value <b>may be locally defined</b>, or one of the following:</p>
                           <ul>
                              
                              
                              <li><strong>asset</strong>: An assessment asset.</li>
                              
                              <li><strong>method</strong>: An assessment method.</li>
                              
                              <li><strong>objective</strong>: Describes a set of control objectives.</li>
                              </ul>
                        </div>
                        </details>
                  </div>
               </div>
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-part/ns" class="toc2 name">ns</h2>
                     <p class="type"><a href="/reference/datatypes/#uri">uri</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-part/ns">Switch to XML</a></div>
                     <p class="formal-name">Part Namespace</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A namespace qualifying the part's name. This allows different organizations to associate
                        distinct semantics with the same name.</p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Provides a means to segment the value space for the <code>name</code>, so that different organizations and individuals can assert control over the allowed
                                 names and associated text used in a part. This allows the semantics associated with
                                 a given name to be defined on an organization-by-organization basis.</p>
                              <p>An organization MUST use a URI that they have control over. e.g., a domain registered
                                 to the organization in a URI, a registered uniform resource names (URN) namespace.</p>
                              <p>When a <code>ns</code> is not provided, its value should be assumed to be <code>http://csrc.nist.gov/ns/oscal</code> and the name should be a name defined by the associated OSCAL model.</p>
                           </div>
                        </details>
                     </div>
                  </div>
               </div>
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-part/class" class="toc2 name">class</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-part/class">Switch to XML</a></div>
                     <p class="formal-name">Part Class</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A textual label that provides a sub-type or characterization of the part's <code>name</code>. This can be used to further distinguish or discriminate between the semantics of
                        multiple parts of the same control with the same <code>name</code> and <code>ns</code>.</p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>A <code>class</code> can be used in validation rules to express extra constraints over named items of
                                 a specific <code>class</code> value.</p>
                              <p>A <code>class</code> can also be used in an OSCAL profile as a means to target an alteration to control
                                 content.</p>
                           </div>
                        </details>
                     </div>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-part/title" class="toc2 name">title</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-part/title">Switch to XML</a></div>
                     <p class="formal-name">Part Title</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A name given to the part, which may be used by a tool for display and navigation.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-part/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-part/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-part/prose" class="toc2 name">prose</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-part/prose">Switch to XML</a></div>
                     <p class="formal-name">Part Text</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Permits multiple paragraphs, lists, tables etc.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-part/parts" class="toc2 name">assessment-part</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-part/part">Switch to XML</a></div>
                     <p class="formal-name">Assessment Part</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">part</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">parts</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>A <code>part</code> provides for logical partitioning of prose, and can be thought of as a grouping structure
                                 (e.g., section). A <code>part</code> can have child parts allowing for arbitrary nesting of prose content (e.g., statement
                                 hierarchy). A <code>part</code> can contain <code>prop</code> objects that allow for enriching prose text with structured name/value information.</p>
                              <p>A <code>part</code> can be assigned an optional <code>id</code>, which allows for internal and external references to the textual concept contained
                                 within a <code>part</code>. A <code>id</code> provides a means for an OSCAL profile, or a higher layer OSCAL model to reference
                                 a specific part within a <code>catalog</code>. For example, an <code>id</code> can be used to reference or to make modifications to a control statement in a profile.</p>
                              <p>Use of <code>part</code> and <code>prop</code> provides for a wide degree of extensibility within the OSCAL catalog model. The optional
                                 <code>ns</code> provides a means to qualify a part's <code>name</code>, allowing for organization-specific vocabularies to be defined with clear semantics.
                                 Any organization that extends OSCAL in this way should consistently assign a <code>ns</code> value that represents the organization, making a given namespace qualified <code>name</code> unique to that organization. This allows the combination of <code>ns</code> and <code>name</code> to always be unique and unambiguous, even when mixed with extensions from other organizations.
                                 Each organization is responsible for governance of their own extensions, and is strongly
                                 encouraged to publish their extensions as standards to their user community. If no
                                 <code>ns</code> is provided, the name is expected to be in the "OSCAL" namespace.</p>
                              <p>To ensure a <code>ns</code> is unique to an organization and naming conflicts are avoided, a URI containing a
                                 DNS or other globally defined organization name should be used. For example, if FedRAMP
                                 and DoD both extend OSCAL, FedRAMP will use the <code>ns</code> "https://fedramp.gov", while DoD will use the <code>ns</code> "https://defense.gov" for any organization specific <code>name</code>.</p>
                              <p>Tools that process OSCAL content are not required to interpret unrecognized OSCAL
                                 extensions; however, OSCAL compliant tools should not modify or remove unrecognized
                                 extensions, unless there is a compelling reason to do so, such as data sensitivity.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-assessment-common/assessment-part">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/assessment-part/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/assessment-part/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-catalog-common/part" class="toc1 name">part</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/part">Switch to XML</a></div>
         <p class="formal-name">Part</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A partition of a control's definition or a child of another part.</p>
         <div class="remarks-group usa-prose">
            <details open="open">
               <summary class="subhead">Remarks</summary>
               <div class="remarks">
                  <p>A <code>part</code> provides for logical partitioning of prose, and can be thought of as a grouping structure
                     (e.g., section). A <code>part</code> can have child parts allowing for arbitrary nesting of prose content (e.g., statement
                     hierarchy). A <code>part</code> can contain <code>prop</code> objects that allow for enriching prose text with structured name/value information.</p>
                  <p>A <code>part</code> can be assigned an optional <code>id</code>, which allows for internal and external references to the textual concept contained
                     within a <code>part</code>. A <code>id</code> provides a means for an OSCAL profile, or a higher layer OSCAL model to reference
                     a specific part within a <code>catalog</code>. For example, an <code>id</code> can be used to reference or to make modifications to a control statement in a profile.</p>
                  <p>Use of <code>part</code> and <code>prop</code> provides for a wide degree of extensibility within the OSCAL catalog model. The optional
                     <code>ns</code> provides a means to qualify a part's <code>name</code>, allowing for organization-specific vocabularies to be defined with clear semantics.
                     Any organization that extends OSCAL in this way should consistently assign a <code>ns</code> value that represents the organization, making a given namespace qualified <code>name</code> unique to that organization. This allows the combination of <code>ns</code> and <code>name</code> to always be unique and unambiguous, even when mixed with extensions from other organizations.
                     Each organization is responsible for governance of their own extensions, and is strongly
                     encouraged to publish their extensions as standards to their user community. If no
                     <code>ns</code> is provided, the name is expected to be in the "OSCAL" namespace.</p>
                  <p>To ensure a <code>ns</code> is unique to an organization and naming conflicts are avoided, a URI containing a
                     DNS or other globally defined organization name should be used. For example, if FedRAMP
                     and DoD both extend OSCAL, FedRAMP will use the <code>ns</code> "https://fedramp.gov", while DoD will use the <code>ns</code> "https://defense.gov" for any organization specific <code>name</code>. </p>
                  <p>Tools that process OSCAL content are not required to interpret unrecognized OSCAL
                     extensions; however, OSCAL compliant tools should not modify or remove unrecognized
                     extensions, unless there is a compelling reason to do so, such as data sensitivity.</p>
               </div>
            </details>
         </div>
         <details>
            <summary>Constraint (1)</summary>
            
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">prop[has-oscal-namespace('http://csrc.nist.gov/ns/oscal')]/@name</code></p>
               <p>The value <b>must</b> be one of the following:</p>
               <ul>
                  
                  <li><strong>label</strong>: A human-readable label for the parent context, which may be rendered in place of
                     the actual identifier for some use cases.</li>
                  
                  <li><strong>sort-id</strong>: An alternative identifier, whose value is easily sortable among other such values
                     in the document.</li>
                  
                  <li><strong>alt-identifier</strong>: An alternate or aliased identifier for the parent context.</li>
                  
                  </ul>
            </div>
            </details>
         <details open="open">
            <summary>Properties (9)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/part/id" class="toc2 name">id</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/part/id">Switch to XML</a></div>
                     <p class="formal-name">Part Identifier</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#human-oriented">human-oriented</a>, <a href="/concepts/identifier-use/#locally-unique">locally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this defined part elsewhere in <a href="/concepts/identifier-use/#scope">this or other OSCAL instances</a>. When referenced from another OSCAL instance, this identifier must be referenced
                        in the context of the containing resource (e.g., import-profile). This id should be
                        assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                        of the document.</p>
                  </div>
               </div>
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/part/name" class="toc2 name">name</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/part/name">Switch to XML</a></div>
                     <p class="formal-name">Part Name</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A textual label that uniquely identifies the part's semantic type.</p>
                  </div>
               </div>
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/part/ns" class="toc2 name">ns</h2>
                     <p class="type"><a href="/reference/datatypes/#uri">uri</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/part/ns">Switch to XML</a></div>
                     <p class="formal-name">Part Namespace</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A namespace qualifying the part's name. This allows different organizations to associate
                        distinct semantics with the same name.</p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Provides a means to segment the value space for the <code>name</code>, so that different organizations and individuals can assert control over the allowed
                                 names and associated text used in a part. This allows the semantics associated with
                                 a given name to be defined on an organization-by-organization basis.</p>
                              <p>An organization MUST use a URI that they have control over. e.g., a domain registered
                                 to the organization in a URI, a registered uniform resource names (URN) namespace.</p>
                              <p>When a <code>ns</code> is not provided, its value should be assumed to be <code>http://csrc.nist.gov/ns/oscal</code> and the name should be a name defined by the associated OSCAL model.</p>
                           </div>
                        </details>
                     </div>
                  </div>
               </div>
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/part/class" class="toc2 name">class</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/part/class">Switch to XML</a></div>
                     <p class="formal-name">Part Class</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A textual label that provides a sub-type or characterization of the part's <code>name</code>. This can be used to further distinguish or discriminate between the semantics of
                        multiple parts of the same control with the same <code>name</code> and <code>ns</code>. </p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>A <code>class</code> can be used in validation rules to express extra constraints over named items of
                                 a specific <code>class</code> value.</p>
                              <p>A <code>class</code> can also be used in an OSCAL profile as a means to target an alteration to control
                                 content.</p>
                           </div>
                        </details>
                     </div>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/part/title" class="toc2 name">title</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/part/title">Switch to XML</a></div>
                     <p class="formal-name">Part Title</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A name given to the part, which may be used by a tool for display and navigation.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/part/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/part/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/part/prose" class="toc2 name">prose</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/part/prose">Switch to XML</a></div>
                     <p class="formal-name">Part Text</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Permits multiple paragraphs, lists, tables etc.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/part/parts" class="toc2 name">part</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/part/part">Switch to XML</a></div>
                     <p class="formal-name">Part</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">parts</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>A <code>part</code> provides for logical partitioning of prose, and can be thought of as a grouping structure
                                 (e.g., section). A <code>part</code> can have child parts allowing for arbitrary nesting of prose content (e.g., statement
                                 hierarchy). A <code>part</code> can contain <code>prop</code> objects that allow for enriching prose text with structured name/value information.</p>
                              <p>A <code>part</code> can be assigned an optional <code>id</code>, which allows for internal and external references to the textual concept contained
                                 within a <code>part</code>. A <code>id</code> provides a means for an OSCAL profile, or a higher layer OSCAL model to reference
                                 a specific part within a <code>catalog</code>. For example, an <code>id</code> can be used to reference or to make modifications to a control statement in a profile.</p>
                              <p>Use of <code>part</code> and <code>prop</code> provides for a wide degree of extensibility within the OSCAL catalog model. The optional
                                 <code>ns</code> provides a means to qualify a part's <code>name</code>, allowing for organization-specific vocabularies to be defined with clear semantics.
                                 Any organization that extends OSCAL in this way should consistently assign a <code>ns</code> value that represents the organization, making a given namespace qualified <code>name</code> unique to that organization. This allows the combination of <code>ns</code> and <code>name</code> to always be unique and unambiguous, even when mixed with extensions from other organizations.
                                 Each organization is responsible for governance of their own extensions, and is strongly
                                 encouraged to publish their extensions as standards to their user community. If no
                                 <code>ns</code> is provided, the name is expected to be in the "OSCAL" namespace.</p>
                              <p>To ensure a <code>ns</code> is unique to an organization and naming conflicts are avoided, a URI containing a
                                 DNS or other globally defined organization name should be used. For example, if FedRAMP
                                 and DoD both extend OSCAL, FedRAMP will use the <code>ns</code> "https://fedramp.gov", while DoD will use the <code>ns</code> "https://defense.gov" for any organization specific <code>name</code>. </p>
                              <p>Tools that process OSCAL content are not required to interpret unrecognized OSCAL
                                 extensions; however, OSCAL compliant tools should not modify or remove unrecognized
                                 extensions, unless there is a compelling reason to do so, such as data sensitivity.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-catalog-common/part">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-catalog-common/part/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-catalog-common/part/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-metadata/party" class="toc1 name">party</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/party">Switch to XML</a></div>
         <p class="formal-name">Party (organization or person)</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A responsible entity which is either a person or an organization.</p>
         <details>
            <summary>Constraint (1)</summary>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">prop/@name</code></p>
               <p>The value <b>must</b> be one of the following:</p>
               <ul>
                  
                  <li><strong>mail-stop</strong>: A mail stop associated with the party.</li>
                  
                  <li><strong>office</strong>: The name or number of the party's office.</li>
                  
                  <li><strong>job-title</strong>: The formal job title of a person.</li>
                  </ul>
            </div>
            </details>
         <details open="open">
            <summary>Properties (12)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/party/uuid" class="toc2 name">uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/party/uuid">Switch to XML</a></div>
                     <p class="formal-name">Party Universally Unique Identifier</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this defined party elsewhere in <a href="/concepts/identifier-use/#scope">this or other OSCAL instances</a>. The locally defined <em>UUID</em> of the <code>party</code> can be used to reference the data item locally or globally (e.g., from an importing
                        OSCAL instance). This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                        of the document.</p>
                  </div>
               </div>
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/party/type" class="toc2 name">type</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/party/type">Switch to XML</a></div>
                     <p class="formal-name">Party Type</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A category describing the kind of party the object describes.</p>
                     <details>
                        <summary>Constraint (1)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>person</strong>: An individual.</li>
                              
                              <li><strong>organization</strong>: A group of individuals formed for a specific purpose.</li>
                              </ul>
                        </div>
                        </details>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/party/name" class="toc2 name">name</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/party/name">Switch to XML</a></div>
                     <p class="formal-name">Party Name</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> The full name of the party. This is typically the legal name associated with the
                        party.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/party/short-name" class="toc2 name">short-name</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/party/short-name">Switch to XML</a></div>
                     <p class="formal-name">Party Short Name</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A short common name, abbreviation, or acronym for the party.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/party/external-ids" class="toc2 name">external-id</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/party/external-id">Switch to XML</a></div>
                     <p class="formal-name">Party External Identifier</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> An identifier for a person or organization using a designated scheme. e.g. an Open
                        Researcher and Contributor ID (ORCID)</p>
                     <p><span class="usa-tag">value key</span> <code class="name">id</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">external-ids</code></p>
                     <details open="open">
                        <summary>Properties (2)</summary>
                        <div class="model field-model">
                           <div class="model-entry definition define-flag">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-metadata/party/external-ids/scheme" class="toc3 name">scheme</h3>
                                 <p class="type"><a href="/reference/datatypes/#uri">uri</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/party/external-id/scheme">Switch to XML</a></div>
                                 <p class="formal-name">External Identifier Schema</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> Indicates the type of external identifier.</p>
                                 <details>
                                    <summary>Constraint (1)</summary>
                                    
                                    <div class="constraint">
                                       <p><span class="usa-tag">allowed value</span></p>
                                       <p>The value <b>may be locally defined</b>, or the following:</p>
                                       <ul>
                                          
                                          <li><strong>https://orcid.org/</strong>: The identifier is Open Researcher and Contributor ID (ORCID).</li>
                                          </ul>
                                    </div>
                                    </details>
                              </div>
                           </div>
                           <div class="model-entry definition m:define-flag">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-metadata/party/external-ids/id" class="toc3 name">id</h3>
                                 <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/party/external-id">Switch to XML</a></div>
                                 <p class="formal-name">Party External Identifier Value</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> This property provides the (nominal) value for this object as a whole.</p>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/party/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/party/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/party/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/party/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/party/email-addresses" class="toc2 name">email-address</h2>
                     <p class="type"><a href="/reference/datatypes/#email">email</a></p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/party/email-address">Switch to XML</a></div>
                     <p class="formal-name">Email Address</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">email-addresses</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>This is a contact email associated with the party.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/field/oscal-metadata/email-address">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/party/telephone-numbers" class="toc2 name">telephone-number</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/party/telephone-number">Switch to XML</a></div>
                     <p class="formal-name">Telephone Number</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">telephone-numbers</code></p>
                     <p><span class="usa-tag">value key</span> <code class="name">number</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>A phone number used to contact the party.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/field/oscal-metadata/telephone-number">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/party/addresses" class="toc2 name">address</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/party/address">Switch to XML</a></div>
                     <p class="formal-name">Address</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">addresses</code></p>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/address">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/party/location-uuids" class="toc2 name">location-uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/party/location-uuid">Switch to XML</a></div>
                     <p class="formal-name">Location Reference</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">location-uuids</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>See the <a href="/concepts/identifier-use/#scope">Concepts - Identifier Use</a> page for additional information about the referenced identifier's scope.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/field/oscal-metadata/location-uuid">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/party/member-of-organizations" class="toc2 name">member-of-organization</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/party/member-of-organization">Switch to XML</a></div>
                     <p class="formal-name">Organizational Affiliation</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a> identifier reference to another <code>party</code> (<code>person</code> or <code>organization</code>) that this subject is associated with. The <em>UUID</em> of the <code>party</code> in the source OSCAL instance is sufficient to reference the data item locally or
                        globally (e.g., in an imported OSCAL instance). </p>
                     <p><span class="usa-tag">group as</span> <code class="name">member-of-organizations</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Parties of both the <code>person</code> or <code>organization</code> type can be associated with an organization using the <code>member-of-organization</code>.</p>
                           </div>
                        </details>
                     </div>
                     <details>
                        <summary>Constraint (1)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">index has key</span>this value must correspond to a listing in the index <code>index-metadata-party-organizations-uuid</code> using a key constructed of key field(s) <code>.</code></p>
                        </div>
                        </details>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/party/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/party/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-field">
      <div class="definition-header">
         <h1 id="/field/oscal-metadata/party-uuid" class="toc1 name">party-uuid</h1>
         <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-metadata/party-uuid">Switch to XML</a></div>
         <p class="formal-name">Party Reference</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a> identifier reference to another <code>party</code> defined in <code>metadata</code>. The <em>UUID</em> of the <code>party</code> in the source OSCAL instance is sufficient to reference the data item locally or
            globally (e.g., in an imported OSCAL instance). </p>
         <div class="remarks-group usa-prose">
            <details open="open">
               <summary class="subhead">Remarks</summary>
               <div class="remarks">
                  <p>See the <a href="/concepts/identifier-use/#scope">Concepts - Identifier Use</a> page for additional information about the referenced identifier's scope.</p>
               </div>
            </details>
         </div>
         <details>
            <summary>Constraint (1)</summary>
            
            <div class="constraint">
               <p><span class="usa-tag">index has key</span>this value must correspond to a listing in the index <code>index-metadata-party-uuid</code> using a key constructed of key field(s) <code>.</code></p>
            </div>
            </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-implementation-common/port-range" class="toc1 name">port-range</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/port-range">Switch to XML</a></div>
         <p class="formal-name">Port Range</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Where applicable this is the IPv4 port range on which the service operates.</p>
         <div class="remarks-group usa-prose">
            <details open="open">
               <summary class="subhead">Remarks</summary>
               <div class="remarks">
                  <p>To be validated as a natural number (integer &gt;= 1). A single port uses the same value
                     for start and end. Use multiple 'port-range' entries for non-contiguous ranges.</p>
               </div>
            </details>
         </div>
         <details open="open">
            <summary>Properties (3)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/port-range/start" class="toc2 name">start</h2>
                     <p class="type"><a href="/reference/datatypes/#nonnegativeinteger">nonNegativeInteger</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/port-range/start">Switch to XML</a></div>
                     <p class="formal-name">Start</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Indicates the starting port number in a port range</p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Should be a number within a permitted range</p>
                           </div>
                        </details>
                     </div>
                  </div>
               </div>
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/port-range/end" class="toc2 name">end</h2>
                     <p class="type"><a href="/reference/datatypes/#nonnegativeinteger">nonNegativeInteger</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/port-range/end">Switch to XML</a></div>
                     <p class="formal-name">End</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Indicates the ending port number in a port range</p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Should be a number within a permitted range</p>
                           </div>
                        </details>
                     </div>
                  </div>
               </div>
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/port-range/transport" class="toc2 name">transport</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/port-range/transport">Switch to XML</a></div>
                     <p class="formal-name">Transport</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Indicates the transport type.</p>
                     <details>
                        <summary>Constraint (1)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span></p>
                           <p>The value <b>must</b> be one of the following:</p>
                           <ul>
                              
                              <li><strong>TCP</strong>: Transmission Control Protocol</li>
                              
                              <li><strong>UDP</strong>: User Datagram Protocol</li>
                              </ul>
                        </div>
                        </details>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-metadata/property" class="toc1 name">prop</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/property">Switch to XML</a></div>
         <p class="formal-name">Property</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> An attribute, characteristic, or quality of the containing object expressed as a
            namespace qualified name/value pair. The value of a property is a simple scalar value,
            which may be expressed as a list of values.</p>
         <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
         <div class="remarks-group usa-prose">
            <details open="open">
               <summary class="subhead">Remarks</summary>
               <div class="remarks">
                  <p>Properties permit the deployment and management of arbitrary controlled values, within
                     OSCAL objects. A property can be included for any purpose useful to an application
                     or implementation. Typically, properties will be used to sort, filter, select, order,
                     and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                     an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                     lexical composition of properties may be constrained by external processes to ensure
                     consistency.</p>
                  <p>Property allows for associated remarks that describe why the specific property value
                     was applied to the containing object, or the significance of the value in the context
                     of the containing object.</p>
               </div>
            </details>
         </div>
         <details open="open">
            <summary>Properties (6)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/property/name" class="toc2 name">name</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/property/name">Switch to XML</a></div>
                     <p class="formal-name">Property Name</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A textual label that uniquely identifies a specific attribute, characteristic, or
                        quality of the property's containing object.</p>
                     <details>
                        <summary>Constraint (1)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed value</span></p>
                           <p>The value <b>may be locally defined</b>, or the following:</p>
                           <ul>
                              
                              <li><strong>marking</strong>: A label or descriptor that is tied to a sensitivity or classification marking system.
                                 An optional class can be used to define the specific marking system used for the associated
                                 value.</li>
                              </ul>
                        </div>
                        </details>
                  </div>
               </div>
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/property/uuid" class="toc2 name">uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/property/uuid">Switch to XML</a></div>
                     <p class="formal-name">Property Universally Unique Identifier</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this defined property elsewhere in <a href="/concepts/identifier-use/#scope">this or other OSCAL instances</a>. This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                        of the document.</p>
                  </div>
               </div>
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/property/ns" class="toc2 name">ns</h2>
                     <p class="type"><a href="/reference/datatypes/#uri">uri</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/property/ns">Switch to XML</a></div>
                     <p class="formal-name">Property Namespace</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A namespace qualifying the property's name. This allows different organizations to
                        associate distinct semantics with the same name.</p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Provides a means to segment the value space for the <code>name</code>, so that different organizations and individuals can assert control over the allowed
                                 names and associated values used in a property. This allows the semantics associated
                                 with a given name/value pair to be defined on an organization-by-organization basis.</p>
                              <p>An organization MUST use a URI that they have control over. e.g., a domain registered
                                 to the organization in a URI, a registered uniform resource names (URN) namespace.</p>
                              <p>When a <code>ns</code> is not provided, its value should be assumed to be <code>http://csrc.nist.gov/ns/oscal</code> and the name should be a name defined by the associated OSCAL model.</p>
                           </div>
                        </details>
                     </div>
                  </div>
               </div>
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/property/value" class="toc2 name">value</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/property/value">Switch to XML</a></div>
                     <p class="formal-name">Property Value</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Indicates the value of the attribute, characteristic, or quality.</p>
                  </div>
               </div>
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/property/class" class="toc2 name">class</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/property/class">Switch to XML</a></div>
                     <p class="formal-name">Property Class</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A textual label that provides a sub-type or characterization of the property's <code>name</code>. This can be used to further distinguish or discriminate between the semantics of
                        multiple properties of the same object with the same <code>name</code> and <code>ns</code>. </p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>A <code>class</code> can be used in validation rules to express extra constraints over named items of
                                 a specific <code>class</code> value.</p>
                           </div>
                        </details>
                     </div>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/property/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/property/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-implementation-common/protocol" class="toc1 name">protocol</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/protocol">Switch to XML</a></div>
         <p class="formal-name">Service Protocol Information</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Information about the protocol used to provide a service.</p>
         <details open="open">
            <summary>Properties (4)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/protocol/uuid" class="toc2 name">uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/protocol/uuid">Switch to XML</a></div>
                     <p class="formal-name">Service Protocol Information Universally Unique Identifier</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this service protocol information elsewhere in
                        <a href="/concepts/identifier-use/#scope">this or other OSCAL instances</a>. The locally defined <em>UUID</em> of the <code>service protocol</code> can be used to reference the data item locally or globally (e.g., in an imported
                        OSCAL instance). This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                        of the document.</p>
                  </div>
               </div>
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/protocol/name" class="toc2 name">name</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/protocol/name">Switch to XML</a></div>
                     <p class="formal-name">Protocol Name</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> The common name of the protocol, which should be the appropriate "service name" from
                        the <a href="https://www.iana.org/assignments/service-names-port-numbers/service-names-port-numbers.xhtml">IANA Service Name and Transport Protocol Port Number Registry</a>. </p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>The short name of the protocol (e.g., https).</p>
                           </div>
                        </details>
                     </div>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/protocol/title" class="toc2 name">title</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/protocol/title">Switch to XML</a></div>
                     <p class="formal-name">Protocol Title</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A human readable name for the protocol (e.g., Transport Layer Security).</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/protocol/port-ranges" class="toc2 name">port-range</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/protocol/port-range">Switch to XML</a></div>
                     <p class="formal-name">Port Range</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">port-ranges</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To be validated as a natural number (integer &gt;= 1). A single port uses the same value
                                 for start and end. Use multiple 'port-range' entries for non-contiguous ranges.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-implementation-common/port-range">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-field">
      <div class="definition-header">
         <h1 id="/field/oscal-metadata/published" class="toc1 name">published</h1>
         <p class="type"><a href="/reference/datatypes/#datetime-with-timezone">dateTime-with-timezone</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-metadata/published">Switch to XML</a></div>
         <p class="formal-name">Publication Timestamp</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> The date and time the document was published. The date-time value must be formatted
            according to <a href="https://tools.ietf.org/html/rfc3339">RFC 3339</a> with full time and time zone included.</p>
         <div class="remarks-group usa-prose">
            <details open="open">
               <summary class="subhead">Remarks</summary>
               <div class="remarks">
                  <p>This value represents the point in time when the OSCAL document was published. Typically,
                     this date value will be machine generated at the time the containing document is published.</p>
                  <p>In some cases, an OSCAL document may be derived from some source material in a different
                     format. In such a case, the <code>published</code> value should indicate when the OSCAL document was published, not the source material.
                     Where necessary, the publication date of the original source material can be captured
                     as a named property or custom metadata construct.</p>
                  <p>A publisher of OSCAL content can use this data point along with its siblings <code>last-modified</code> and <code>version</code> to establish a sequence of successive revisions of a given OSCAL-based publication.
                     The metadata for previous revisions can be represented as a <code>revision</code> in this object.</p>
               </div>
            </details>
         </div>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-assessment-common/related-task" class="toc1 name">related-task</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/related-task">Switch to XML</a></div>
         <p class="formal-name">Task Reference</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Identifies an individual task for which the containing object is a consequence of.</p>
         <details>
            <summary>Constraint (1)</summary>
            
            <div class="constraint">
               <p><span class="usa-tag">is unique</span> for <code class="path">responsible-party</code>: any target value must be unique (i.e., occur only once)</p>
            </div>
            </details>
         <details open="open">
            <summary>Properties (7)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/related-task/task-uuid" class="toc2 name">task-uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/related-task/task-uuid">Switch to XML</a></div>
                     <p class="formal-name">Task Universally Unique Identifier Reference</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a> identifier reference to a unique task.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/related-task/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/related-task/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/related-task/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/related-task/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/related-task/responsible-parties" class="toc2 name">responsible-party</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/related-task/responsible-party">Switch to XML</a></div>
                     <p class="formal-name">Responsible Party</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">responsible-parties</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Identifies the person or organization responsible for performing a specific role defined
                                 by the activity.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/responsible-party">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/related-task/subjects" class="toc2 name">subject</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/related-task/subject">Switch to XML</a></div>
                     <p class="formal-name">Subject of Assessment</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">subject</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">subjects</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Processing of an include/exclude pair starts with processing the include, then removing
                                 matching entries in the exclude.</p>
                           </div>
                           <div class="remarks">
                              <p>The assessment subjects that the task was performed against.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-assessment-common/assessment-subject">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/related-task/identified-subject" class="toc2 name">identified-subject</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/related-task/identified-subject">Switch to XML</a></div>
                     <p class="formal-name">Identified Subject</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Used to detail assessment subjects that were identfied by this task.</p>
                     <details open="open">
                        <summary>Properties (2)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition define-flag">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/related-task/identified-subject/subject-placeholder-uuid" class="toc3 name">subject-placeholder-uuid</h3>
                                 <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/related-task/identified-subject/subject-placeholder-uuid">Switch to XML</a></div>
                                 <p class="formal-name">Assessment Subject Placeholder Universally Unique Identifier Reference</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a> identifier reference to a unique assessment subject placeholder defined by this task.</p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/related-task/identified-subject/subjects" class="toc3 name">subject</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[1 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/related-task/identified-subject/subject">Switch to XML</a></div>
                                 <p class="formal-name">Subject of Assessment</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">use name</span> <code class="name">subject</code></p>
                                 <p><span class="usa-tag">group as</span> <code class="name">subjects</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>Processing of an include/exclude pair starts with processing the include, then removing
                                             matching entries in the exclude.</p>
                                       </div>
                                       <div class="remarks">
                                          <p>The assessment subjects that the task identified, which will be used by another task
                                             through a subject-placeholder reference. Such a task will "consume" these subjects.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-assessment-common/assessment-subject">See definition</a></p>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/related-task/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/related-task/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-field">
      <div class="definition-header">
         <h1 id="/field/oscal-metadata/remarks" class="toc1 name">remarks</h1>
         <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-metadata/remarks">Switch to XML</a></div>
         <p class="formal-name">Remarks</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Additional commentary on the containing object.</p>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-assessment-common/response" class="toc1 name">response</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/response">Switch to XML</a></div>
         <p class="formal-name">Risk Response</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Describes either recommended or an actual plan for addressing the risk.</p>
         <details>
            <summary>Constraints (2)</summary>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed value</span> for <code class="path">prop/@name</code></p>
               <p>The value <b>may be locally defined</b>, or the following:</p>
               <ul>
                  
                  <li><strong>type</strong></li>
                  </ul>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">prop[@name='type']/@value</code></p>
               <p>The value <b>may be locally defined</b>, or one of the following:</p>
               <ul>
                  
                  <li><strong>avoid</strong>: The risk will be eliminated.</li>
                  
                  <li><strong>mitigate</strong>: The risk will be reduced.</li>
                  
                  <li><strong>transfer</strong>: The risk will be transferred to another organization or entity.</li>
                  
                  <li><strong>accept</strong>: The risk will continue to exist without further efforts to address it. (Sometimes
                     referred to as "Operationally required")</li>
                  
                  <li><strong>share</strong>: The risk will be partially transferred to another organization or entity.</li>
                  
                  <li><strong>contingency</strong>: Plans will be made to address the risk impact if the risk occurs. (This is a form
                     of mitigation.)</li>
                  
                  <li><strong>none</strong>: No response, such as when the identified risk is found to be a false positive.</li>
                  </ul>
            </div>
            </details>
         <details open="open">
            <summary>Properties (10)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/response/uuid" class="toc2 name">uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/response/uuid">Switch to XML</a></div>
                     <p class="formal-name">Remediation Universally Unique Identifier</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this remediation elsewhere in <a href="/concepts/identifier-use/#scope">this or other OSCAL instances</a>. The locally defined <em>UUID</em> of the <code>risk response</code> can be used to reference the data item locally or globally (e.g., in an imported
                        OSCAL instance). This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                        of the document.</p>
                  </div>
               </div>
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/response/lifecycle" class="toc2 name">lifecycle</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/response/lifecycle">Switch to XML</a></div>
                     <p class="formal-name">Remediation Intent</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Identifies whether this is a recommendation, such as from an assessor or tool, or
                        an actual plan accepted by the system owner.</p>
                     <details>
                        <summary>Constraint (1)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span></p>
                           <p>The value <b>may be locally defined</b>, or one of the following:</p>
                           <ul>
                              
                              <li><strong>recommendation</strong>: Recommended Remediation</li>
                              
                              <li><strong>planned</strong>: The actions intended to resolve the risk.</li>
                              
                              <li><strong>completed</strong>: This remediation activities were performed to address the risk.</li>
                              </ul>
                        </div>
                        </details>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/response/title" class="toc2 name">title</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/response/title">Switch to XML</a></div>
                     <p class="formal-name">Response Title</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> The title for this response activity.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/response/description" class="toc2 name">description</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/response/description">Switch to XML</a></div>
                     <p class="formal-name">Response Description</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A human-readable description of this response plan.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/response/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/response/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/response/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/response/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/response/origins" class="toc2 name">origin</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/response/origin">Switch to XML</a></div>
                     <p class="formal-name">Origin</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">origins</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Used to identify the individual and/or tool that generated this recommended or planned
                                 response.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-assessment-common/origin">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/response/required-assets" class="toc2 name">required-asset</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/response/required-asset">Switch to XML</a></div>
                     <p class="formal-name">Required Asset</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Identifies an asset required to achieve remediation.</p>
                     <p><span class="usa-tag">group as</span> <code class="name">required-assets</code></p>
                     <details open="open">
                        <summary>Properties (7)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition define-flag">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/response/required-assets/uuid" class="toc3 name">uuid</h3>
                                 <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/response/required-asset/uuid">Switch to XML</a></div>
                                 <p class="formal-name">Required Universally Unique Identifier</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this required asset elsewhere in <a href="/concepts/identifier-use/#scope">this or other OSCAL instances</a>. The locally defined <em>UUID</em> of the <code>asset</code> can be used to reference the data item locally or globally (e.g., in an imported
                                    OSCAL instance). This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                                    of the document.</p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/response/required-assets/subjects" class="toc3 name">subject</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/response/required-asset/subject">Switch to XML</a></div>
                                 <p class="formal-name">Identifies the Subject</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">use name</span> <code class="name">subject</code></p>
                                 <p><span class="usa-tag">group as</span> <code class="name">subjects</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>The subject reference UUID could point to an item defined in the SSP, AP, or AR.</p>
                                          <p>Tools should check look for the ID in every file imported directly or indirectly.</p>
                                       </div>
                                       <div class="remarks">
                                          <p>Identifies an asset associated with this requirement, such as a party, system component,
                                             or inventory-item.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-assessment-common/subject-reference">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition define-field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/response/required-assets/title" class="toc3 name">title</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/response/required-asset/title">Switch to XML</a></div>
                                 <p class="formal-name">Title for Required Asset</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> The title for this required asset.</p>
                              </div>
                           </div>
                           <div class="model-entry definition define-field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/response/required-assets/description" class="toc3 name">description</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                 <p class="occurrence">[1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/response/required-asset/description">Switch to XML</a></div>
                                 <p class="formal-name">Description of Required Asset</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A human-readable description of this required asset.</p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/response/required-assets/props" class="toc3 name">property</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/response/required-asset/prop">Switch to XML</a></div>
                                 <p class="formal-name">Property</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                                 <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>Properties permit the deployment and management of arbitrary controlled values, within
                                             OSCAL objects. A property can be included for any purpose useful to an application
                                             or implementation. Typically, properties will be used to sort, filter, select, order,
                                             and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                             an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                             lexical composition of properties may be constrained by external processes to ensure
                                             consistency.</p>
                                          <p>Property allows for associated remarks that describe why the specific property value
                                             was applied to the containing object, or the significance of the value in the context
                                             of the containing object.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/response/required-assets/links" class="toc3 name">link</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/response/required-asset/link">Switch to XML</a></div>
                                 <p class="formal-name">Link</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                             a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                                          <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/response/required-assets/remarks" class="toc3 name">remarks</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/response/required-asset/remarks">Switch to XML</a></div>
                                 <p class="formal-name">Remarks</p>
                              </div>
                              <div class="body">
                                 <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/response/tasks" class="toc2 name">task</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/response/task">Switch to XML</a></div>
                     <p class="formal-name">Task</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">tasks</code></p>
                     <p class="definition-link"><a href="#/assembly/oscal-assessment-common/task">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/response/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/response/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-metadata/responsible-party" class="toc1 name">responsible-party</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/responsible-party">Switch to XML</a></div>
         <p class="formal-name">Responsible Party</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A reference to a set of organizations or persons that have responsibility for performing
            a referenced role in the context of the containing object.</p>
         <details>
            <summary>Constraints (2)</summary>
            
            <div class="constraint">
               <p><span class="usa-tag">index has key</span>this value must correspond to a listing in the index <code>index-metadata-role-id</code> using a key constructed of key field(s) <code>@role-id</code></p>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">index has key</span> for <code class="path">party-uuid</code>this value must correspond to a listing in the index <code>index-metadata-party-uuid</code> using a key constructed of key field(s) <code>.</code></p>
            </div>
            </details>
         <details open="open">
            <summary>Properties (5)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/responsible-party/role-id" class="toc2 name">role-id</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/responsible-party/role-id">Switch to XML</a></div>
                     <p class="formal-name">Responsible Role</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#human-oriented">human-oriented</a> identifier reference to <code>roles</code> served by the user.</p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/responsible-party/party-uuids" class="toc2 name">party-uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[1 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/responsible-party/party-uuid">Switch to XML</a></div>
                     <p class="formal-name">Party Reference</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">party-uuids</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>See the <a href="/concepts/identifier-use/#scope">Concepts - Identifier Use</a> page for additional information about the referenced identifier's scope.</p>
                           </div>
                           <div class="remarks">
                              <p>Specifies one or more parties that are responsible for performing the associated <code>role</code>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/field/oscal-metadata/party-uuid">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/responsible-party/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/responsible-party/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/responsible-party/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/responsible-party/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/responsible-party/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/responsible-party/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-metadata/responsible-role" class="toc1 name">responsible-role</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/responsible-role">Switch to XML</a></div>
         <p class="formal-name">Responsible Role</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A reference to one or more roles with responsibility for performing a function relative
            to the containing object.</p>
         <details open="open">
            <summary>Properties (5)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/responsible-role/role-id" class="toc2 name">role-id</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/responsible-role/role-id">Switch to XML</a></div>
                     <p class="formal-name">Responsible Role ID</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#human-oriented">human-oriented</a> identifier reference to <code>roles</code> responsible for the business function.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/responsible-role/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/responsible-role/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/responsible-role/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/responsible-role/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/responsible-role/party-uuids" class="toc2 name">party-uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/responsible-role/party-uuid">Switch to XML</a></div>
                     <p class="formal-name">Party Reference</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">party-uuids</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>See the <a href="/concepts/identifier-use/#scope">Concepts - Identifier Use</a> page for additional information about the referenced identifier's scope.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/field/oscal-metadata/party-uuid">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/responsible-role/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/responsible-role/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-ar/result" class="toc1 name">result</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result">Switch to XML</a></div>
         <p class="formal-name">Assessment Result</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Used by the assessment results and POA&amp;M. In the assessment results, this identifies
            all of the assessment observations and findings, initial and residual risks, deviations,
            and disposition. In the POA&amp;M, this identifies initial and residual risks, deviations,
            and disposition.</p>
         <details open="open">
            <summary>Properties (15)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/result/uuid" class="toc2 name">uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/uuid">Switch to XML</a></div>
                     <p class="formal-name">Results Universally Unique Identifier</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this set of results in <a href="/concepts/identifier-use/#ar-identifiers">this or other OSCAL instances</a>. The locally defined <em>UUID</em> of the <code>assessment result</code> can be used to reference the data item locally or globally (e.g., in an imported
                        OSCAL instance). This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                        of the document.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/result/title" class="toc2 name">title</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/title">Switch to XML</a></div>
                     <p class="formal-name">Results Title</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> The title for this set of results.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/result/description" class="toc2 name">description</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/description">Switch to XML</a></div>
                     <p class="formal-name">Results Description</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A human-readable description of this set of test results.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/result/start" class="toc2 name">start</h2>
                     <p class="type"><a href="/reference/datatypes/#datetime-with-timezone">dateTime-with-timezone</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/start">Switch to XML</a></div>
                     <p class="formal-name">start field</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Date/time stamp identifying the start of the evidence collection reflected in these
                        results.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/result/end" class="toc2 name">end</h2>
                     <p class="type"><a href="/reference/datatypes/#datetime-with-timezone">dateTime-with-timezone</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/end">Switch to XML</a></div>
                     <p class="formal-name">end field</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Date/time stamp identifying the end of the evidence collection reflected in these
                        results. In a continuous motoring scenario, this may contain the same value as start
                        if appropriate.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/result/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/result/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/result/local-definitions" class="toc2 name">local-definitions</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/local-definitions">Switch to XML</a></div>
                     <p class="formal-name">Local Definitions</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Used to define data objects that are used in the assessment plan, that do not appear
                        in the referenced SSP.</p>
                     <details>
                        <summary>Constraints (2)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">is unique</span> for <code class="path">component</code>: any target value must be unique (i.e., occur only once)</p>
                        </div>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">is unique</span> for <code class="path">user</code>: any target value must be unique (i.e., occur only once)</p>
                        </div>
                        </details>
                     <details open="open">
                        <summary>Properties (5)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-ar/result/local-definitions/components" class="toc3 name">component</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/local-definitions/component">Switch to XML</a></div>
                                 <p class="formal-name">Component</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">use name</span> <code class="name">component</code></p>
                                 <p><span class="usa-tag">group as</span> <code class="name">components</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>Components may be products, services, application programming interface (APIs), policies,
                                             processes, plans, guidance, standards, or other tangible items that enable security
                                             and/or privacy.</p>
                                          <p>The <code>type</code> indicates which of these component types is represented.</p>
                                          <p>When defining a <code>service</code> component where are relationship to other components is known, one or more <code>link</code> entries with rel values of provided-by and used-by can be used to link to the specific
                                             component identifier(s) that provide and use the service respectively.</p>
                                       </div>
                                       <div class="remarks">
                                          <p>Used to add any components, not defined via the System Security Plan (AR-&gt;AP-&gt;SSP)</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-implementation-common/system-component">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-ar/result/local-definitions/inventory-items" class="toc3 name">inventory-item</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/local-definitions/inventory-item">Switch to XML</a></div>
                                 <p class="formal-name">Inventory Item</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">group as</span> <code class="name">inventory-items</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>Used to add any inventory-items, not defined via the System Security Plan (AR-&gt;AP-&gt;SSP)</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-implementation-common/inventory-item">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-ar/result/local-definitions/users" class="toc3 name">user</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/local-definitions/user">Switch to XML</a></div>
                                 <p class="formal-name">System User</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">use name</span> <code class="name">user</code></p>
                                 <p><span class="usa-tag">group as</span> <code class="name">users</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>Permissible values to be determined closer to the application, such as by a receiving
                                             authority.</p>
                                       </div>
                                       <div class="remarks">
                                          <p>Used to add any users, not defined via the System Security Plan (AR-&gt;AP-&gt;SSP)</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-implementation-common/system-user">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-ar/result/local-definitions/assessment-assets" class="toc3 name">assessment-assets</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/local-definitions/assessment-assets">Switch to XML</a></div>
                                 <p class="formal-name">Assessment Assets</p>
                              </div>
                              <div class="body">
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>This needs to be defined in the results if an assessment platform used is different
                                             from the one described in the assessment plan. Else the platform(s) defined in the
                                             plan may be referenced within the results.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-assessment-common/assessment-assets">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-ar/result/local-definitions/tasks" class="toc3 name">assessment-task</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/local-definitions/assessment-task">Switch to XML</a></div>
                                 <p class="formal-name">Task</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">use name</span> <code class="name">assessment-task</code></p>
                                 <p><span class="usa-tag">group as</span> <code class="name">tasks</code></p>
                                 <p class="definition-link"><a href="#/assembly/oscal-assessment-common/task">See definition</a></p>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/result/reviewed-controls" class="toc2 name">reviewed-controls</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/reviewed-controls">Switch to XML</a></div>
                     <p class="formal-name">Reviewed Controls and Control Objectives</p>
                  </div>
                  <div class="body">
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>In the context of an assessment plan, this construct is used to identify the controls
                                 and control objectives that are to be assessed. In the context of an assessment result,
                                 this construct is used to identify the actual controls and objectives that were assessed,
                                 reflecting any changes from the plan.</p>
                              <p>When resolving the selection of controls and control objectives, the following processing
                                 will occur:</p>
                              <p>1. Controls will be resolved by creating a set of controls based on the control-selections
                                 by first handling the includes, and then removing any excluded controls.</p>
                              <p>2. The set of control objectives will be resolved from the set of controls that was
                                 generated in the previous step. The set of control objectives is based on the control-objective-selection
                                 by first handling the includes, and then removing any excluded control objectives.</p>
                           </div>
                           <div class="remarks">
                              <p>The Assessment Results <code>control-selection</code> ignores any control selection in the Assessment Plan and re-selects controls from
                                 the baseline identified by the SSP.</p>
                              <p>The Assessment Results <code>control-objective-selection</code> ignores any control objective selection in the Assessment Plan and re-selects control
                                 objectives from the baseline identified by the SSP.</p>
                              <p>Any additional control objectives defined in the Assessment Plan <code>local-definitions</code> do not need to be re-defined in the Assessment Results <code>local-definitions</code>; however, if they were explicitly referenced with an Assessment Plan <code>control-objective-selection</code>, they need to be selected again in the Assessment Results <code>control-objective-selection</code>.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-assessment-common/reviewed-controls">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/result/attestations" class="toc2 name">attestation</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/attestation">Switch to XML</a></div>
                     <p class="formal-name">Attestation Statements</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A set of textual statements, typically written by the assessor.</p>
                     <p><span class="usa-tag">group as</span> <code class="name">attestations</code></p>
                     <details>
                        <summary>Constraint (1)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">is unique</span> for <code class="path">responsible-party</code>: any target value must be unique (i.e., occur only once)</p>
                        </div>
                        </details>
                     <details open="open">
                        <summary>Properties (2)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-ar/result/attestations/responsible-parties" class="toc3 name">responsible-party</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/attestation/responsible-party">Switch to XML</a></div>
                                 <p class="formal-name">Responsible Party</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">group as</span> <code class="name">responsible-parties</code></p>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/responsible-party">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-ar/result/attestations/parts" class="toc3 name">part</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[1 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/attestation/part">Switch to XML</a></div>
                                 <p class="formal-name">Assessment Part</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">use name</span> <code class="name">part</code></p>
                                 <p><span class="usa-tag">group as</span> <code class="name">parts</code></p>
                                 <p><span class="usa-tag">use name</span> <code class="name">part</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>A <code>part</code> provides for logical partitioning of prose, and can be thought of as a grouping structure
                                             (e.g., section). A <code>part</code> can have child parts allowing for arbitrary nesting of prose content (e.g., statement
                                             hierarchy). A <code>part</code> can contain <code>prop</code> objects that allow for enriching prose text with structured name/value information.</p>
                                          <p>A <code>part</code> can be assigned an optional <code>id</code>, which allows for internal and external references to the textual concept contained
                                             within a <code>part</code>. A <code>id</code> provides a means for an OSCAL profile, or a higher layer OSCAL model to reference
                                             a specific part within a <code>catalog</code>. For example, an <code>id</code> can be used to reference or to make modifications to a control statement in a profile.</p>
                                          <p>Use of <code>part</code> and <code>prop</code> provides for a wide degree of extensibility within the OSCAL catalog model. The optional
                                             <code>ns</code> provides a means to qualify a part's <code>name</code>, allowing for organization-specific vocabularies to be defined with clear semantics.
                                             Any organization that extends OSCAL in this way should consistently assign a <code>ns</code> value that represents the organization, making a given namespace qualified <code>name</code> unique to that organization. This allows the combination of <code>ns</code> and <code>name</code> to always be unique and unambiguous, even when mixed with extensions from other organizations.
                                             Each organization is responsible for governance of their own extensions, and is strongly
                                             encouraged to publish their extensions as standards to their user community. If no
                                             <code>ns</code> is provided, the name is expected to be in the "OSCAL" namespace.</p>
                                          <p>To ensure a <code>ns</code> is unique to an organization and naming conflicts are avoided, a URI containing a
                                             DNS or other globally defined organization name should be used. For example, if FedRAMP
                                             and DoD both extend OSCAL, FedRAMP will use the <code>ns</code> "https://fedramp.gov", while DoD will use the <code>ns</code> "https://defense.gov" for any organization specific <code>name</code>.</p>
                                          <p>Tools that process OSCAL content are not required to interpret unrecognized OSCAL
                                             extensions; however, OSCAL compliant tools should not modify or remove unrecognized
                                             extensions, unless there is a compelling reason to do so, such as data sensitivity.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-assessment-common/assessment-part">See definition</a></p>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/result/assessment-log" class="toc2 name">assessment-log</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/assessment-log">Switch to XML</a></div>
                     <p class="formal-name">Assessment Log</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A log of all assessment-related actions taken.</p>
                     <details open="open">
                        <summary>Property (1)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition define-assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-ar/result/assessment-log/entries" class="toc3 name">entry</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[1 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/assessment-log/entry">Switch to XML</a></div>
                                 <p class="formal-name">Assessment Log Entry</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> Identifies the result of an action and/or task that occurred as part of executing
                                    an assessment plan or an assessment event that occurred in producing the assessment
                                    results.</p>
                                 <p><span class="usa-tag">group as</span> <code class="name">entries</code></p>
                                 <details open="open">
                                    <summary>Properties (10)</summary>
                                    <div class="model assembly-model">
                                       <div class="model-entry definition define-flag">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-ar/result/assessment-log/entries/uuid" class="toc4 name">uuid</h4>
                                             <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                                             <p class="occurrence">[0 or 1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/assessment-log/entry/uuid">Switch to XML</a></div>
                                             <p class="formal-name">Assessment Log Entry Universally Unique Identifier</p>
                                          </div>
                                          <div class="body">
                                             <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference an assessment event in <a href="/concepts/identifier-use/#ar-identifiers">this or other OSCAL instances</a>. The locally defined <em>UUID</em> of the <code>assessment log entry</code> can be used to reference the data item locally or globally (e.g., in an imported
                                                OSCAL instance). This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                                                of the document.</p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition define-field">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-ar/result/assessment-log/entries/title" class="toc4 name">title</h4>
                                             <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                                             <p class="occurrence">[0 or 1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/assessment-log/entry/title">Switch to XML</a></div>
                                             <p class="formal-name">Action Title</p>
                                          </div>
                                          <div class="body">
                                             <p class="description"><span class="usa-tag">description</span> The title for this event.</p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition define-field">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-ar/result/assessment-log/entries/description" class="toc4 name">description</h4>
                                             <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                             <p class="occurrence">[0 or 1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/assessment-log/entry/description">Switch to XML</a></div>
                                             <p class="formal-name">Action Description</p>
                                          </div>
                                          <div class="body">
                                             <p class="description"><span class="usa-tag">description</span> A human-readable description of this event.</p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition define-field">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-ar/result/assessment-log/entries/start" class="toc4 name">start</h4>
                                             <p class="type"><a href="/reference/datatypes/#datetime-with-timezone">dateTime-with-timezone</a></p>
                                             <p class="occurrence">[1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/assessment-log/entry/start">Switch to XML</a></div>
                                             <p class="formal-name">Start</p>
                                          </div>
                                          <div class="body">
                                             <p class="description"><span class="usa-tag">description</span> Identifies the start date and time of an event.</p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition define-field">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-ar/result/assessment-log/entries/end" class="toc4 name">end</h4>
                                             <p class="type"><a href="/reference/datatypes/#datetime-with-timezone">dateTime-with-timezone</a></p>
                                             <p class="occurrence">[0 or 1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/assessment-log/entry/end">Switch to XML</a></div>
                                             <p class="formal-name">End</p>
                                          </div>
                                          <div class="body">
                                             <p class="description"><span class="usa-tag">description</span> Identifies the end date and time of an event. If the event is a point in time, the
                                                start and end will be the same date and time.</p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition assembly">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-ar/result/assessment-log/entries/props" class="toc4 name">property</h4>
                                             <p class="type">assembly<br class="br" /> </p>
                                             <p class="occurrence">[0 to ∞]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/assessment-log/entry/prop">Switch to XML</a></div>
                                             <p class="formal-name">Property</p>
                                          </div>
                                          <div class="body">
                                             <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                                             <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                                             <div class="remarks-group usa-prose">
                                                <details open="open">
                                                   <summary class="subhead">Remarks</summary>
                                                   <div class="remarks">
                                                      <p>Properties permit the deployment and management of arbitrary controlled values, within
                                                         OSCAL objects. A property can be included for any purpose useful to an application
                                                         or implementation. Typically, properties will be used to sort, filter, select, order,
                                                         and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                                         an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                                         lexical composition of properties may be constrained by external processes to ensure
                                                         consistency.</p>
                                                      <p>Property allows for associated remarks that describe why the specific property value
                                                         was applied to the containing object, or the significance of the value in the context
                                                         of the containing object.</p>
                                                   </div>
                                                </details>
                                             </div>
                                             <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition assembly">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-ar/result/assessment-log/entries/links" class="toc4 name">link</h4>
                                             <p class="type">assembly<br class="br" /> </p>
                                             <p class="occurrence">[0 to ∞]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/assessment-log/entry/link">Switch to XML</a></div>
                                             <p class="formal-name">Link</p>
                                          </div>
                                          <div class="body">
                                             <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                                             <div class="remarks-group usa-prose">
                                                <details open="open">
                                                   <summary class="subhead">Remarks</summary>
                                                   <div class="remarks">
                                                      <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                                         a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                                                      <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                                                   </div>
                                                </details>
                                             </div>
                                             <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition assembly">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-ar/result/assessment-log/entries/logged-by" class="toc4 name">logged-by</h4>
                                             <p class="type">assembly<br class="br" /> </p>
                                             <p class="occurrence">[0 to ∞]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/assessment-log/entry/logged-by">Switch to XML</a></div>
                                             <p class="formal-name">Logged By</p>
                                          </div>
                                          <div class="body">
                                             <p><span class="usa-tag">group as</span> <code class="name">logged-by</code></p>
                                             <p class="definition-link"><a href="#/assembly/oscal-assessment-common/logged-by">See definition</a></p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition assembly">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-ar/result/assessment-log/entries/related-tasks" class="toc4 name">related-task</h4>
                                             <p class="type">assembly<br class="br" /> </p>
                                             <p class="occurrence">[0 to ∞]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/assessment-log/entry/related-task">Switch to XML</a></div>
                                             <p class="formal-name">Task Reference</p>
                                          </div>
                                          <div class="body">
                                             <p><span class="usa-tag">group as</span> <code class="name">related-tasks</code></p>
                                             <p class="definition-link"><a href="#/assembly/oscal-assessment-common/related-task">See definition</a></p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition field">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-ar/result/assessment-log/entries/remarks" class="toc4 name">remarks</h4>
                                             <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                             <p class="occurrence">[0 or 1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/assessment-log/entry/remarks">Switch to XML</a></div>
                                             <p class="formal-name">Remarks</p>
                                          </div>
                                          <div class="body">
                                             <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                                          </div>
                                       </div>
                                    </div>
                                 </details>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/result/observations" class="toc2 name">observation</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/observation">Switch to XML</a></div>
                     <p class="formal-name">Observation</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">observations</code></p>
                     <p class="definition-link"><a href="#/assembly/oscal-assessment-common/observation">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/result/risks" class="toc2 name">risk</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/risk">Switch to XML</a></div>
                     <p class="formal-name">Identified Risk</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">risks</code></p>
                     <p class="definition-link"><a href="#/assembly/oscal-assessment-common/risk">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/result/findings" class="toc2 name">finding</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/finding">Switch to XML</a></div>
                     <p class="formal-name">Finding</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">findings</code></p>
                     <p class="definition-link"><a href="#/assembly/oscal-ar/finding">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-ar/result/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-ar/result/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-assessment-common/reviewed-controls" class="toc1 name">reviewed-controls</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/reviewed-controls">Switch to XML</a></div>
         <p class="formal-name">Reviewed Controls and Control Objectives</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Identifies the controls being assessed and their control objectives.</p>
         <div class="remarks-group usa-prose">
            <details open="open">
               <summary class="subhead">Remarks</summary>
               <div class="remarks">
                  <p>In the context of an assessment plan, this construct is used to identify the controls
                     and control objectives that are to be assessed. In the context of an assessment result,
                     this construct is used to identify the actual controls and objectives that were assessed,
                     reflecting any changes from the plan.</p>
                  <p>When resolving the selection of controls and control objectives, the following processing
                     will occur:</p>
                  <p>1. Controls will be resolved by creating a set of controls based on the control-selections
                     by first handling the includes, and then removing any excluded controls.</p>
                  <p>2. The set of control objectives will be resolved from the set of controls that was
                     generated in the previous step. The set of control objectives is based on the control-objective-selection
                     by first handling the includes, and then removing any excluded control objectives.</p>
               </div>
            </details>
         </div>
         <details open="open">
            <summary>Properties (6)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/reviewed-controls/description" class="toc2 name">description</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/reviewed-controls/description">Switch to XML</a></div>
                     <p class="formal-name">Control Objective Description</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A human-readable description of control objectives.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/reviewed-controls/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/reviewed-controls/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/reviewed-controls/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/reviewed-controls/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/reviewed-controls/control-selections" class="toc2 name">control-selection</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[1 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/reviewed-controls/control-selection">Switch to XML</a></div>
                     <p class="formal-name">Assessed Controls</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Identifies the controls being assessed. In the assessment plan, these are the planned
                        controls. In the assessment results, these are the actual controls, and reflects any
                        changes from the plan.</p>
                     <p><span class="usa-tag">group as</span> <code class="name">control-selections</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>The <code>include-all</code>, specifies all control identified in the <strong>baseline</strong> are included in the scope if this assessment, as specified by the <code>include-profile</code> statement within the linked SSP.</p>
                              <p>Any control specified within <code>exclude-controls</code> must first be within a range of explicitly included controls, via <code>include-controls</code> or <code>include-all</code>.</p>
                           </div>
                        </details>
                     </div>
                     <details open="open">
                        <summary>Properties (6)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition define-field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/reviewed-controls/control-selections/description" class="toc3 name">description</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/reviewed-controls/control-selection/description">Switch to XML</a></div>
                                 <p class="formal-name">Assessed Controls Description</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A human-readable description of in-scope controls specified for assessment.</p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/reviewed-controls/control-selections/props" class="toc3 name">property</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/reviewed-controls/control-selection/prop">Switch to XML</a></div>
                                 <p class="formal-name">Property</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                                 <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>Properties permit the deployment and management of arbitrary controlled values, within
                                             OSCAL objects. A property can be included for any purpose useful to an application
                                             or implementation. Typically, properties will be used to sort, filter, select, order,
                                             and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                             an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                             lexical composition of properties may be constrained by external processes to ensure
                                             consistency.</p>
                                          <p>Property allows for associated remarks that describe why the specific property value
                                             was applied to the containing object, or the significance of the value in the context
                                             of the containing object.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/reviewed-controls/control-selections/links" class="toc3 name">link</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/reviewed-controls/control-selection/link">Switch to XML</a></div>
                                 <p class="formal-name">Link</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                             a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                                          <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/reviewed-controls/control-selections/include-all" class="toc3 name">include-all</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/reviewed-controls/control-selection/include-all">Switch to XML</a></div>
                                 <p class="formal-name">Include All</p>
                              </div>
                              <div class="body">
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>This element provides an alternative to calling controls individually from a catalog.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-catalog-common/include-all">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/reviewed-controls/control-selections/include-controls" class="toc3 name">include-control</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[1 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/reviewed-controls/control-selection/include-control">Switch to XML</a></div>
                                 <p class="formal-name">Select Control</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">use name</span> <code class="name">include-control</code></p>
                                 <p><span class="usa-tag">group as</span> <code class="name">include-controls</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>Used to select a control for inclusion by the control's identifier. Specific control
                                             statements can be selected by their statement identifier.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-assessment-common/select-control-by-id">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/reviewed-controls/control-selections/exclude-controls" class="toc3 name">exclude-control</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/reviewed-controls/control-selection/exclude-control">Switch to XML</a></div>
                                 <p class="formal-name">Select Control</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">use name</span> <code class="name">exclude-control</code></p>
                                 <p><span class="usa-tag">group as</span> <code class="name">exclude-controls</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>Used to select a control for exclusion by the control's identifier. Specific control
                                             statements can be excluded by their statement identifier.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-assessment-common/select-control-by-id">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/reviewed-controls/control-selections/remarks" class="toc3 name">remarks</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/reviewed-controls/control-selection/remarks">Switch to XML</a></div>
                                 <p class="formal-name">Remarks</p>
                              </div>
                              <div class="body">
                                 <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/reviewed-controls/control-objective-selections" class="toc2 name">control-objective-selection</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/reviewed-controls/control-objective-selection">Switch to XML</a></div>
                     <p class="formal-name">Referenced Control Objectives</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Identifies the control objectives of the assessment. In the assessment plan, these
                        are the planned objectives. In the assessment results, these are the assessed objectives,
                        and reflects any changes from the plan.</p>
                     <p><span class="usa-tag">group as</span> <code class="name">control-objective-selections</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>The <code>include-all</code> field, specifies all control objectives for any in-scope control. In-scope controls
                                 are defined in the <code>control-selection</code>.</p>
                              <p>Any control objective specified within <code>exclude-controls</code> must first be within a range of explicitly included control objectives, via <code>include-objectives</code> or <code>include-all</code>.</p>
                           </div>
                        </details>
                     </div>
                     <details open="open">
                        <summary>Properties (6)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition define-field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/reviewed-controls/control-objective-selections/description" class="toc3 name">description</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/reviewed-controls/control-objective-selection/description">Switch to XML</a></div>
                                 <p class="formal-name">Control Objectives Description</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A human-readable description of this collection of control objectives.</p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/reviewed-controls/control-objective-selections/props" class="toc3 name">property</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/reviewed-controls/control-objective-selection/prop">Switch to XML</a></div>
                                 <p class="formal-name">Property</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                                 <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>Properties permit the deployment and management of arbitrary controlled values, within
                                             OSCAL objects. A property can be included for any purpose useful to an application
                                             or implementation. Typically, properties will be used to sort, filter, select, order,
                                             and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                             an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                             lexical composition of properties may be constrained by external processes to ensure
                                             consistency.</p>
                                          <p>Property allows for associated remarks that describe why the specific property value
                                             was applied to the containing object, or the significance of the value in the context
                                             of the containing object.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/reviewed-controls/control-objective-selections/links" class="toc3 name">link</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/reviewed-controls/control-objective-selection/link">Switch to XML</a></div>
                                 <p class="formal-name">Link</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                             a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                                          <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/reviewed-controls/control-objective-selections/include-all" class="toc3 name">include-all</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/reviewed-controls/control-objective-selection/include-all">Switch to XML</a></div>
                                 <p class="formal-name">Include All</p>
                              </div>
                              <div class="body">
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>This element provides an alternative to calling controls individually from a catalog.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-catalog-common/include-all">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/reviewed-controls/control-objective-selections/include-objectives" class="toc3 name">include-objective</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[1 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/reviewed-controls/control-objective-selection/include-objective">Switch to XML</a></div>
                                 <p class="formal-name">Select Objective</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">use name</span> <code class="name">include-objective</code></p>
                                 <p><span class="usa-tag">group as</span> <code class="name">include-objectives</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>Used to select a control objective for inclusion by the control objective's identifier.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-assessment-common/select-objective-by-id">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/reviewed-controls/control-objective-selections/exclude-objectives" class="toc3 name">exclude-objective</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/reviewed-controls/control-objective-selection/exclude-objective">Switch to XML</a></div>
                                 <p class="formal-name">Select Objective</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">use name</span> <code class="name">exclude-objective</code></p>
                                 <p><span class="usa-tag">group as</span> <code class="name">exclude-objectives</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>Used to select a control objective for exclusion by the control objective's identifier.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-assessment-common/select-objective-by-id">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/reviewed-controls/control-objective-selections/remarks" class="toc3 name">remarks</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/reviewed-controls/control-objective-selection/remarks">Switch to XML</a></div>
                                 <p class="formal-name">Remarks</p>
                              </div>
                              <div class="body">
                                 <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/reviewed-controls/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/reviewed-controls/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-metadata/revision" class="toc1 name">revision</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/revision">Switch to XML</a></div>
         <p class="formal-name">Revision History Entry</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> An entry in a sequential list of revisions to the containing document in reverse
            chronological order (i.e., most recent previous revision first).</p>
         <div class="remarks-group usa-prose">
            <details open="open">
               <summary class="subhead">Remarks</summary>
               <div class="remarks">
                  <p>While <code>published</code>, <code>last-modified</code>, <code>oscal-version</code>, and <code>version</code> are not required, values for these entries should be provided if the information
                     is known. For a revision entry to be considered valid, at least one of the following
                     items must be provided: <code>published</code>, <code>last-modified</code>, <code>version</code>, or a <code>link</code> with a <code>rel</code> of <q>source</q>.</p>
               </div>
            </details>
         </div>
         <details>
            <summary>Constraint (1)</summary>
            
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">link/@rel</code></p>
               <p>The value <b>may be locally defined</b>, or one of the following:</p>
               <ul>
                  
                  <li><strong>canonical</strong>: The link identifies the authoritative location for this file. Defined by RFC 6596.</li>
                  
                  <li><strong>alternate</strong>: The link identifies an alternative location or format for this file. Defined by
                     the HTML Living Standard</li>
                  
                  <li><strong>predecessor-version</strong>: This link identifies a resource containing the predecessor version in the version
                     history. Defined by  RFC 5829.</li>
                  
                  <li><strong>successor-version</strong>: This link identifies a resource containing the predecessor version in the version
                     history. Defined by RFC 5829.</li>
                  </ul>
            </div>
            </details>
         <details open="open">
            <summary>Properties (8)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/revision/title" class="toc2 name">title</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/revision/title">Switch to XML</a></div>
                     <p class="formal-name">Document Title</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A name given to the document revision, which may be used by a tool for display and
                        navigation.</p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/revision/published" class="toc2 name">published</h2>
                     <p class="type"><a href="/reference/datatypes/#datetime-with-timezone">dateTime-with-timezone</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/revision/published">Switch to XML</a></div>
                     <p class="formal-name">Publication Timestamp</p>
                  </div>
                  <div class="body">
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>This value represents the point in time when the OSCAL document was published. Typically,
                                 this date value will be machine generated at the time the containing document is published.</p>
                              <p>In some cases, an OSCAL document may be derived from some source material in a different
                                 format. In such a case, the <code>published</code> value should indicate when the OSCAL document was published, not the source material.
                                 Where necessary, the publication date of the original source material can be captured
                                 as a named property or custom metadata construct.</p>
                              <p>A publisher of OSCAL content can use this data point along with its siblings <code>last-modified</code> and <code>version</code> to establish a sequence of successive revisions of a given OSCAL-based publication.
                                 The metadata for previous revisions can be represented as a <code>revision</code> in this object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/field/oscal-metadata/published">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/revision/last-modified" class="toc2 name">last-modified</h2>
                     <p class="type"><a href="/reference/datatypes/#datetime-with-timezone">dateTime-with-timezone</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/revision/last-modified">Switch to XML</a></div>
                     <p class="formal-name">Last Modified Timestamp</p>
                  </div>
                  <div class="body">
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>This value represents the point in time when the OSCAL document was last updated,
                                 or at the point of creation the creation date. Typically, this date value will be
                                 machine generated at time of creation or modification.</p>
                              <p>In some cases, an OSCAL document may be derived from some source material in a different
                                 format. In such a case, the <code>last-modified</code> value should indicate the modification time of the OSCAL document, not the source
                                 material.</p>
                              <p>A publisher of OSCAL content can use this data point along with its siblings <code>published</code> and <code>version</code> to establish a sequence of successive revisions of a given OSCAL-based publication.
                                 The metadata for previous revisions can be represented as a <code>revision</code> in this object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/field/oscal-metadata/last-modified">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/revision/version" class="toc2 name">version</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/revision/version">Switch to XML</a></div>
                     <p class="formal-name">Document Version</p>
                  </div>
                  <div class="body">
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>A version string may be a release number, sequence number, date, or other identifier
                                 suffcient to distinguish between different document versions. This version is typically
                                 set by the document owner or by the tool used to maintain the content.</p>
                              <p>While not required, it is recommended that OSCAL content authors use <a href="https://semver.org/spec/v2.0.0.html">Semantic Versioning</a> as a format for version strings. This allows for the easy identification of a version
                                 tree consisting of major, minor, and patch numbers.</p>
                              <p>A publisher of OSCAL content can use this data point along with its siblings <code>published</code> and <code>last-modified</code> to establish a sequence of successive revisions of a given OSCAL-based publication.
                                 The metadata for previous revisions can be represented as a <code>revision</code> in this object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/field/oscal-metadata/version">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/revision/oscal-version" class="toc2 name">oscal-version</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/revision/oscal-version">Switch to XML</a></div>
                     <p class="formal-name">OSCAL version</p>
                  </div>
                  <div class="body">
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Indicates the version of the OSCAL model to which this data set conforms, for example
                                 <q>1.1.0</q> or <q>1.0.0-M1</q>. That can be used as a hint by a tool to indicate which version of the OSCAL XML
                                 or JSON schema to use for validation.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/field/oscal-metadata/oscal-version">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/revision/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/revision/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/revision/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/revision/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/revision/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/revision/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-assessment-common/risk" class="toc1 name">risk</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk">Switch to XML</a></div>
         <p class="formal-name">Identified Risk</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> An identified risk.</p>
         <details>
            <summary>Constraints (2)</summary>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">prop/@name</code></p>
               <p>The value <b>must</b> be one of the following:</p>
               <ul>
                  
                  <li><strong>false-positive</strong>: The risk has been confirmed to be a false positive.</li>
                  
                  <li><strong>accepted</strong>: The risk has been accepted. No further action will be taken.</li>
                  
                  <li><strong>risk-adjusted</strong>: The risk has been adjusted.</li>
                  
                  <li><strong>priority</strong>: A numeric value indicating the sequence in which risks should be addressed. (Lower
                     numbers are higher priority)</li>
                  </ul>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">matches</span> for <code class="path">prop[@name='priority']/@value</code>: the target value must match the lexical form of the 'integer' data type.</p>
            </div>
            </details>
         <details open="open">
            <summary>Properties (15)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/risk/uuid" class="toc2 name">uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/uuid">Switch to XML</a></div>
                     <p class="formal-name">Risk Universally Unique Identifier</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this risk elsewhere in <a href="/concepts/identifier-use/#scope">this or other OSCAL instances</a>. The locally defined <em>UUID</em> of the <code>risk</code> can be used to reference the data item locally or globally (e.g., in an imported
                        OSCAL instance). This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                        of the document.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/risk/title" class="toc2 name">title</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/title">Switch to XML</a></div>
                     <p class="formal-name">Risk Title</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> The title for this risk.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/risk/description" class="toc2 name">description</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/description">Switch to XML</a></div>
                     <p class="formal-name">Risk Description</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A human-readable summary of the identified risk, to include a statement of how the
                        risk impacts the system.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/risk/statement" class="toc2 name">statement</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/statement">Switch to XML</a></div>
                     <p class="formal-name">Risk Statement</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> An summary of impact for how the risk affects the system.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/risk/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/risk/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/risk/status" class="toc2 name">status</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/status">Switch to XML</a></div>
                     <p class="formal-name">Risk Status</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">status</code></p>
                     <p class="definition-link"><a href="#/field/oscal-assessment-common/risk-status">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/risk/origins" class="toc2 name">origin</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/origin">Switch to XML</a></div>
                     <p class="formal-name">Origin</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">origins</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Used to identify the individual and/or tool that identified this risk.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-assessment-common/origin">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/risk/threat-ids" class="toc2 name">threat-id</h2>
                     <p class="type"><a href="/reference/datatypes/#uri">uri</a></p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/threat-id">Switch to XML</a></div>
                     <p class="formal-name">Threat ID</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">value key</span> <code class="name">id</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">threat-ids</code></p>
                     <p class="definition-link"><a href="#/field/oscal-assessment-common/threat-id">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/risk/characterizations" class="toc2 name">characterization</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/characterization">Switch to XML</a></div>
                     <p class="formal-name">Characterization</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">characterizations</code></p>
                     <p class="definition-link"><a href="#/assembly/oscal-assessment-common/characterization">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/risk/mitigating-factors" class="toc2 name">mitigating-factor</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/mitigating-factor">Switch to XML</a></div>
                     <p class="formal-name">Mitigating Factor</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Describes an existing mitigating factor that may affect the overall determination
                        of the risk, with an optional link to an implementation statement in the SSP.</p>
                     <p><span class="usa-tag">group as</span> <code class="name">mitigating-factors</code></p>
                     <details open="open">
                        <summary>Properties (6)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition define-flag">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/risk/mitigating-factors/uuid" class="toc3 name">uuid</h3>
                                 <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/mitigating-factor/uuid">Switch to XML</a></div>
                                 <p class="formal-name">Mitigating Factor Universally Unique Identifier</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this mitigating factor elsewhere in <a href="/concepts/identifier-use/#scope">this or other OSCAL instances</a>. The locally defined <em>UUID</em> of the <code>mitigating factor</code> can be used to reference the data item locally or globally (e.g., in an imported
                                    OSCAL instance). This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                                    of the document.</p>
                              </div>
                           </div>
                           <div class="model-entry definition define-flag">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/risk/mitigating-factors/implementation-uuid" class="toc3 name">implementation-uuid</h3>
                                 <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/mitigating-factor/implementation-uuid">Switch to XML</a></div>
                                 <p class="formal-name">Implementation UUID</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this implementation statement elsewhere in <a href="/concepts/identifier-use/#scope">this or other OSCAL instances</a>s. The locally defined <em>UUID</em> of the <code>implementation statement</code> can be used to reference the data item locally or globally (e.g., in an imported
                                    OSCAL instance). This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                                    of the document.</p>
                              </div>
                           </div>
                           <div class="model-entry definition define-field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/risk/mitigating-factors/description" class="toc3 name">description</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                 <p class="occurrence">[1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/mitigating-factor/description">Switch to XML</a></div>
                                 <p class="formal-name">Mitigating Factor Description</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A human-readable description of this mitigating factor.</p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/risk/mitigating-factors/props" class="toc3 name">property</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/mitigating-factor/prop">Switch to XML</a></div>
                                 <p class="formal-name">Property</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                                 <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>Properties permit the deployment and management of arbitrary controlled values, within
                                             OSCAL objects. A property can be included for any purpose useful to an application
                                             or implementation. Typically, properties will be used to sort, filter, select, order,
                                             and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                             an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                             lexical composition of properties may be constrained by external processes to ensure
                                             consistency.</p>
                                          <p>Property allows for associated remarks that describe why the specific property value
                                             was applied to the containing object, or the significance of the value in the context
                                             of the containing object.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/risk/mitigating-factors/links" class="toc3 name">link</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/mitigating-factor/link">Switch to XML</a></div>
                                 <p class="formal-name">Link</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                             a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                                          <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/risk/mitigating-factors/subjects" class="toc3 name">subject</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/mitigating-factor/subject">Switch to XML</a></div>
                                 <p class="formal-name">Identifies the Subject</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">use name</span> <code class="name">subject</code></p>
                                 <p><span class="usa-tag">group as</span> <code class="name">subjects</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>The subject reference UUID could point to an item defined in the SSP, AP, or AR.</p>
                                          <p>Tools should check look for the ID in every file imported directly or indirectly.</p>
                                       </div>
                                       <div class="remarks">
                                          <p>Links identifiable elements of the system to this mitigating factor, such as an inventory-item
                                             or component.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-assessment-common/subject-reference">See definition</a></p>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/risk/deadline" class="toc2 name">deadline</h2>
                     <p class="type"><a href="/reference/datatypes/#datetime-with-timezone">dateTime-with-timezone</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/deadline">Switch to XML</a></div>
                     <p class="formal-name">Risk Resolution Deadline</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> The date/time by which the risk must be resolved.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/risk/remediations" class="toc2 name">response</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/response">Switch to XML</a></div>
                     <p class="formal-name">Risk Response</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">remediations</code></p>
                     <p class="definition-link"><a href="#/assembly/oscal-assessment-common/response">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/risk/risk-log" class="toc2 name">risk-log</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/risk-log">Switch to XML</a></div>
                     <p class="formal-name">Risk Log</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A log of all risk-related tasks taken.</p>
                     <details open="open">
                        <summary>Property (1)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition define-assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/risk/risk-log/entries" class="toc3 name">entry</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[1 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/risk-log/entry">Switch to XML</a></div>
                                 <p class="formal-name">Risk Log Entry</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> Identifies an individual risk response that occurred as part of managing an identified
                                    risk.</p>
                                 <p><span class="usa-tag">group as</span> <code class="name">entries</code></p>
                                 <details>
                                    <summary>Constraints (2)</summary>
                                    
                                    <div class="constraint">
                                       <p><span class="usa-tag">allowed value</span> for <code class="path">prop/@name</code></p>
                                       <p>The value <b>may be locally defined</b>, or the following:</p>
                                       <ul>
                                          
                                          <li><strong>type</strong>: The type of remediation tracking entry. Can be multi-valued.</li>
                                          </ul>
                                    </div>
                                    
                                    <div class="constraint">
                                       <p><span class="usa-tag">allowed values</span> for <code class="path">prop[@name='type']/@value</code></p>
                                       <p>The value <b>may be locally defined</b>, or one of the following:</p>
                                       <ul>
                                          
                                          <li><strong>vendor-check-in</strong>: Contacted vendor to determine the status of a pending fix to a known vulnerability.</li>
                                          
                                          <li><strong>status-update</strong>: Information related to the current state of response to this risk.</li>
                                          
                                          <li><strong>milestone-complete</strong>: A significant step in the response plan has been achieved.</li>
                                          
                                          <li><strong>mitigation</strong>: An activity was completed that reduces the likelihood or impact of this risk.</li>
                                          
                                          <li><strong>remediated</strong>: An activity was completed that eliminates the likelihood or impact of this risk.</li>
                                          
                                          
                                          <li><strong>closed</strong>: The risk is no longer applicable to the system.</li>
                                          
                                          <li><strong>dr-submission</strong>: A deviation request was made to the authorizing official.</li>
                                          
                                          <li><strong>dr-updated</strong>: A previously submitted deviation request has been modified.</li>
                                          
                                          <li><strong>dr-approved</strong>: The authorizing official approved the deviation.</li>
                                          
                                          <li><strong>dr-rejected</strong>: The authorizing official rejected the deviation.</li>
                                          </ul>
                                    </div>
                                    </details>
                                 <details open="open">
                                    <summary>Properties (11)</summary>
                                    <div class="model assembly-model">
                                       <div class="model-entry definition define-flag">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-assessment-common/risk/risk-log/entries/uuid" class="toc4 name">uuid</h4>
                                             <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                                             <p class="occurrence">[0 or 1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/risk-log/entry/uuid">Switch to XML</a></div>
                                             <p class="formal-name">Risk Log Entry Universally Unique Identifier</p>
                                          </div>
                                          <div class="body">
                                             <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this risk log entry elsewhere in <a href="/concepts/identifier-use/#scope">this or other OSCAL instances</a>. The locally defined <em>UUID</em> of the <code>risk log entry</code> can be used to reference the data item locally or globally (e.g., in an imported
                                                OSCAL instance). This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                                                of the document.</p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition define-field">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-assessment-common/risk/risk-log/entries/title" class="toc4 name">title</h4>
                                             <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                                             <p class="occurrence">[0 or 1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/risk-log/entry/title">Switch to XML</a></div>
                                             <p class="formal-name">Title</p>
                                          </div>
                                          <div class="body">
                                             <p class="description"><span class="usa-tag">description</span> The title for this risk log entry.</p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition define-field">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-assessment-common/risk/risk-log/entries/description" class="toc4 name">description</h4>
                                             <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                             <p class="occurrence">[0 or 1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/risk-log/entry/description">Switch to XML</a></div>
                                             <p class="formal-name">Risk Task Description</p>
                                          </div>
                                          <div class="body">
                                             <p class="description"><span class="usa-tag">description</span> A human-readable description of what was done regarding the risk.</p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition define-field">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-assessment-common/risk/risk-log/entries/start" class="toc4 name">start</h4>
                                             <p class="type"><a href="/reference/datatypes/#datetime-with-timezone">dateTime-with-timezone</a></p>
                                             <p class="occurrence">[1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/risk-log/entry/start">Switch to XML</a></div>
                                             <p class="formal-name">Start</p>
                                          </div>
                                          <div class="body">
                                             <p class="description"><span class="usa-tag">description</span> Identifies the start date and time of the event.</p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition define-field">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-assessment-common/risk/risk-log/entries/end" class="toc4 name">end</h4>
                                             <p class="type"><a href="/reference/datatypes/#datetime-with-timezone">dateTime-with-timezone</a></p>
                                             <p class="occurrence">[0 or 1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/risk-log/entry/end">Switch to XML</a></div>
                                             <p class="formal-name">End</p>
                                          </div>
                                          <div class="body">
                                             <p class="description"><span class="usa-tag">description</span> Identifies the end date and time of the event. If the event is a point in time, the
                                                start and end will be the same date and time.</p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition assembly">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-assessment-common/risk/risk-log/entries/props" class="toc4 name">property</h4>
                                             <p class="type">assembly<br class="br" /> </p>
                                             <p class="occurrence">[0 to ∞]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/risk-log/entry/prop">Switch to XML</a></div>
                                             <p class="formal-name">Property</p>
                                          </div>
                                          <div class="body">
                                             <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                                             <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                                             <div class="remarks-group usa-prose">
                                                <details open="open">
                                                   <summary class="subhead">Remarks</summary>
                                                   <div class="remarks">
                                                      <p>Properties permit the deployment and management of arbitrary controlled values, within
                                                         OSCAL objects. A property can be included for any purpose useful to an application
                                                         or implementation. Typically, properties will be used to sort, filter, select, order,
                                                         and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                                         an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                                         lexical composition of properties may be constrained by external processes to ensure
                                                         consistency.</p>
                                                      <p>Property allows for associated remarks that describe why the specific property value
                                                         was applied to the containing object, or the significance of the value in the context
                                                         of the containing object.</p>
                                                   </div>
                                                </details>
                                             </div>
                                             <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition assembly">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-assessment-common/risk/risk-log/entries/links" class="toc4 name">link</h4>
                                             <p class="type">assembly<br class="br" /> </p>
                                             <p class="occurrence">[0 to ∞]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/risk-log/entry/link">Switch to XML</a></div>
                                             <p class="formal-name">Link</p>
                                          </div>
                                          <div class="body">
                                             <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                                             <div class="remarks-group usa-prose">
                                                <details open="open">
                                                   <summary class="subhead">Remarks</summary>
                                                   <div class="remarks">
                                                      <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                                         a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                                                      <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                                                   </div>
                                                </details>
                                             </div>
                                             <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition assembly">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-assessment-common/risk/risk-log/entries/logged-by" class="toc4 name">logged-by</h4>
                                             <p class="type">assembly<br class="br" /> </p>
                                             <p class="occurrence">[0 to ∞]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/risk-log/entry/logged-by">Switch to XML</a></div>
                                             <p class="formal-name">Logged By</p>
                                          </div>
                                          <div class="body">
                                             <p><span class="usa-tag">group as</span> <code class="name">logged-by</code></p>
                                             <p class="definition-link"><a href="#/assembly/oscal-assessment-common/logged-by">See definition</a></p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition field">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-assessment-common/risk/risk-log/entries/status-change" class="toc4 name">status-change</h4>
                                             <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                                             <p class="occurrence">[0 or 1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/risk-log/entry/status-change">Switch to XML</a></div>
                                             <p class="formal-name">Risk Status</p>
                                          </div>
                                          <div class="body">
                                             <p><span class="usa-tag">use name</span> <code class="name">status-change</code></p>
                                             <div class="remarks-group usa-prose">
                                                <details open="open">
                                                   <summary class="subhead">Remarks</summary>
                                                   <div class="remarks">
                                                      <p>Identifies a change in risk status made resulting from the task described by this
                                                         risk log entry. This allows the risk's status history to be captured as a sequence
                                                         of risk log entries.</p>
                                                   </div>
                                                </details>
                                             </div>
                                             <p class="definition-link"><a href="#/field/oscal-assessment-common/risk-status">See definition</a></p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition define-assembly">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-assessment-common/risk/risk-log/entries/related-responses" class="toc4 name">related-response</h4>
                                             <p class="type">assembly<br class="br" /> </p>
                                             <p class="occurrence">[0 to ∞]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/risk-log/entry/related-response">Switch to XML</a></div>
                                             <p class="formal-name">Risk Response Reference</p>
                                          </div>
                                          <div class="body">
                                             <p class="description"><span class="usa-tag">description</span> Identifies an individual risk response that this log entry is for.</p>
                                             <p><span class="usa-tag">group as</span> <code class="name">related-responses</code></p>
                                             <details open="open">
                                                <summary>Properties (5)</summary>
                                                <div class="model assembly-model">
                                                   <div class="model-entry definition define-flag">
                                                      <div class="instance-header">
                                                         <h5 id="/assembly/oscal-assessment-common/risk/risk-log/entries/related-responses/response-uuid" class="toc5 name">response-uuid</h5>
                                                         <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                                                         <p class="occurrence">[0 or 1]</p>
                                                         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/risk-log/entry/related-response/response-uuid">Switch to XML</a></div>
                                                         <p class="formal-name">Response Universally Unique Identifier Reference</p>
                                                      </div>
                                                      <div class="body">
                                                         <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a> identifier reference to a unique risk response.</p>
                                                      </div>
                                                   </div>
                                                   <div class="model-entry definition assembly">
                                                      <div class="instance-header">
                                                         <h5 id="/assembly/oscal-assessment-common/risk/risk-log/entries/related-responses/props" class="toc5 name">property</h5>
                                                         <p class="type">assembly<br class="br" /> </p>
                                                         <p class="occurrence">[0 to ∞]</p>
                                                         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/risk-log/entry/related-response/prop">Switch to XML</a></div>
                                                         <p class="formal-name">Property</p>
                                                      </div>
                                                      <div class="body">
                                                         <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                                                         <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                                                         <div class="remarks-group usa-prose">
                                                            <details open="open">
                                                               <summary class="subhead">Remarks</summary>
                                                               <div class="remarks">
                                                                  <p>Properties permit the deployment and management of arbitrary controlled values, within
                                                                     OSCAL objects. A property can be included for any purpose useful to an application
                                                                     or implementation. Typically, properties will be used to sort, filter, select, order,
                                                                     and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                                                     an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                                                     lexical composition of properties may be constrained by external processes to ensure
                                                                     consistency.</p>
                                                                  <p>Property allows for associated remarks that describe why the specific property value
                                                                     was applied to the containing object, or the significance of the value in the context
                                                                     of the containing object.</p>
                                                               </div>
                                                            </details>
                                                         </div>
                                                         <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                                                      </div>
                                                   </div>
                                                   <div class="model-entry definition assembly">
                                                      <div class="instance-header">
                                                         <h5 id="/assembly/oscal-assessment-common/risk/risk-log/entries/related-responses/links" class="toc5 name">link</h5>
                                                         <p class="type">assembly<br class="br" /> </p>
                                                         <p class="occurrence">[0 to ∞]</p>
                                                         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/risk-log/entry/related-response/link">Switch to XML</a></div>
                                                         <p class="formal-name">Link</p>
                                                      </div>
                                                      <div class="body">
                                                         <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                                                         <div class="remarks-group usa-prose">
                                                            <details open="open">
                                                               <summary class="subhead">Remarks</summary>
                                                               <div class="remarks">
                                                                  <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                                                     a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                                                                  <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                                                               </div>
                                                            </details>
                                                         </div>
                                                         <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                                                      </div>
                                                   </div>
                                                   <div class="model-entry definition assembly">
                                                      <div class="instance-header">
                                                         <h5 id="/assembly/oscal-assessment-common/risk/risk-log/entries/related-responses/related-tasks" class="toc5 name">related-task</h5>
                                                         <p class="type">assembly<br class="br" /> </p>
                                                         <p class="occurrence">[0 to ∞]</p>
                                                         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/risk-log/entry/related-response/related-task">Switch to XML</a></div>
                                                         <p class="formal-name">Task Reference</p>
                                                      </div>
                                                      <div class="body">
                                                         <p><span class="usa-tag">group as</span> <code class="name">related-tasks</code></p>
                                                         <div class="remarks-group usa-prose">
                                                            <details open="open">
                                                               <summary class="subhead">Remarks</summary>
                                                               <div class="remarks">
                                                                  <p>This is used to identify the task(s) that this log entry was generated for.</p>
                                                               </div>
                                                            </details>
                                                         </div>
                                                         <p class="definition-link"><a href="#/assembly/oscal-assessment-common/related-task">See definition</a></p>
                                                      </div>
                                                   </div>
                                                   <div class="model-entry definition field">
                                                      <div class="instance-header">
                                                         <h5 id="/assembly/oscal-assessment-common/risk/risk-log/entries/related-responses/remarks" class="toc5 name">remarks</h5>
                                                         <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                                         <p class="occurrence">[0 or 1]</p>
                                                         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/risk-log/entry/related-response/remarks">Switch to XML</a></div>
                                                         <p class="formal-name">Remarks</p>
                                                      </div>
                                                      <div class="body">
                                                         <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                                                      </div>
                                                   </div>
                                                </div>
                                             </details>
                                          </div>
                                       </div>
                                       <div class="model-entry definition field">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-assessment-common/risk/risk-log/entries/remarks" class="toc4 name">remarks</h4>
                                             <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                             <p class="occurrence">[0 or 1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/risk-log/entry/remarks">Switch to XML</a></div>
                                             <p class="formal-name">Remarks</p>
                                          </div>
                                          <div class="body">
                                             <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                                          </div>
                                       </div>
                                    </div>
                                 </details>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/risk/related-observations" class="toc2 name">related-observation</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/related-observation">Switch to XML</a></div>
                     <p class="formal-name">Related Observation</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Relates the finding to a set of referenced observations that were used to determine
                        the finding.</p>
                     <p><span class="usa-tag">group as</span> <code class="name">related-observations</code></p>
                     <details open="open">
                        <summary>Property (1)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition define-flag">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/risk/related-observations/observation-uuid" class="toc3 name">observation-uuid</h3>
                                 <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/risk/related-observation/observation-uuid">Switch to XML</a></div>
                                 <p class="formal-name">Observation Universally Unique Identifier Reference</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a> identifier reference to an observation defined in the list of observations.</p>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-field">
      <div class="definition-header">
         <h1 id="/field/oscal-assessment-common/risk-status" class="toc1 name">risk-status</h1>
         <p class="type"><a href="/reference/datatypes/#token">token</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-assessment-common/risk-status">Switch to XML</a></div>
         <p class="formal-name">Risk Status</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Describes the status of the associated risk.</p>
         <details>
            <summary>Constraint (1)</summary>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span></p>
               <p>The value <b>may be locally defined</b>, or one of the following:</p>
               <ul>
                  
                  <li><strong>open</strong>: The risk has been identified.</li>
                  
                  <li><strong>investigating</strong>: The identified risk is being investigated. (Open risk)</li>
                  
                  <li><strong>remediating</strong>: Remediation activities are underway, but are not yet complete. (Open risk)</li>
                  
                  <li><strong>deviation-requested</strong>: A risk deviation, such as false positive, risk reduction, or operational requirement
                     has been submitted for approval. (Open risk)</li>
                  
                  <li><strong>deviation-approved</strong>: A risk deviation, such as false positive, risk reduction, or operational requirement
                     has been approved. (Open risk)</li>
                  
                  <li><strong>closed</strong>: The risk has been resolved.</li>
                  </ul>
            </div>
            </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-metadata/role" class="toc1 name">role</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/role">Switch to XML</a></div>
         <p class="formal-name">Role</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Defines a function assumed or expected to be assumed by a party in a specific situation.</p>
         <div class="remarks-group usa-prose">
            <details open="open">
               <summary class="subhead">Remarks</summary>
               <div class="remarks">
                  <p>Permissible values to be determined closer to the application (e.g. by a receiving
                     authority).</p>
                  <p>OSCAL has defined a set of standardized roles for consistent use in OSCAL documents.
                     This allows tools consuming OSCAL content to infer specific semantics when these roles
                     are used. These roles are documented in the specific contexts of their use (e.g.,
                     responsible-party, responsible-role). When using such a role, it is necessary to define
                     these roles in this list, which will then allow such a role to be referenced.</p>
               </div>
            </details>
         </div>
         <details open="open">
            <summary>Properties (7)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/role/id" class="toc2 name">id</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/role/id">Switch to XML</a></div>
                     <p class="formal-name">Role Identifier</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#human-oriented">human-oriented</a>, <a href="/concepts/identifier-use/#locally-unique">locally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this defined role elsewhere in <a href="/concepts/identifier-use/#scope">this or other OSCAL instances</a>. When referenced from another OSCAL instance, the locally defined <em>ID</em> of the <code>Role</code> from the imported OSCAL instance must be referenced in the context of the containing
                        resource (e.g., import, import-component-definition, import-profile, import-ssp or
                        import-ap). This ID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                        of the document.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/role/title" class="toc2 name">title</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/role/title">Switch to XML</a></div>
                     <p class="formal-name">Role Title</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A name given to the role, which may be used by a tool for display and navigation.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/role/short-name" class="toc2 name">short-name</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/role/short-name">Switch to XML</a></div>
                     <p class="formal-name">Role Short Name</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A short common name, abbreviation, or acronym for the role.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/role/description" class="toc2 name">description</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/role/description">Switch to XML</a></div>
                     <p class="formal-name">Role Description</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A summary of the role's purpose and associated responsibilities.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/role/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/role/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/role/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/role/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-metadata/role/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-metadata/role/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-field">
      <div class="definition-header">
         <h1 id="/field/oscal-metadata/role-id" class="toc1 name">role-id</h1>
         <p class="type"><a href="/reference/datatypes/#token">token</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-metadata/role-id">Switch to XML</a></div>
         <p class="formal-name">Role Identifier Reference</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#human-oriented">human-oriented</a> identifier reference to <code>roles</code> served by the user.</p>
         <details>
            <summary>Constraint (1)</summary>
            
            <div class="constraint">
               <p><span class="usa-tag">index has key</span>this value must correspond to a listing in the index <code>index-metadata-role-id</code> using a key constructed of key field(s) <code>.</code></p>
            </div>
            </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-assessment-common/select-control-by-id" class="toc1 name">select-control-by-id</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/select-control-by-id">Switch to XML</a></div>
         <p class="formal-name">Select Control</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Used to select a control for inclusion/exclusion based on one or more control identifiers.
            A set of statement identifiers can be used to target the inclusion/exclusion to only
            specific control statements providing more granularity over the specific statements
            that are within the asessment scope.</p>
         <details open="open">
            <summary>Properties (2)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/select-control-by-id/control-id" class="toc2 name">control-id</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/select-control-by-id/control-id">Switch to XML</a></div>
                     <p class="formal-name">Control Identifier Reference</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/flag/oscal-catalog-common/control-id">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/select-control-by-id/statement-ids" class="toc2 name">statement-id</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/select-control-by-id/statement-id">Switch to XML</a></div>
                     <p class="formal-name">Include Specific Statements</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Used to constrain the selection to only specificity identified statements.</p>
                     <p><span class="usa-tag">group as</span> <code class="name">statement-ids</code></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-assessment-common/select-objective-by-id" class="toc1 name">select-objective-by-id</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/select-objective-by-id">Switch to XML</a></div>
         <p class="formal-name">Select Objective</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Used to select a control objective for inclusion/exclusion based on the control objective's
            identifier.</p>
         <details open="open">
            <summary>Property (1)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/select-objective-by-id/objective-id" class="toc2 name">objective-id</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/select-objective-by-id/objective-id">Switch to XML</a></div>
                     <p class="formal-name">Objective ID</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/flag/oscal-assessment-common/objective-id">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-assessment-common/select-subject-by-id" class="toc1 name">select-subject-by-id</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/select-subject-by-id">Switch to XML</a></div>
         <p class="formal-name">Select Assessment Subject</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Identifies a set of assessment subjects to include/exclude by UUID.</p>
         <details open="open">
            <summary>Properties (5)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/select-subject-by-id/subject-uuid" class="toc2 name">subject-uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/select-subject-by-id/subject-uuid">Switch to XML</a></div>
                     <p class="formal-name">Subject Universally Unique Identifier Reference</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/flag/oscal-assessment-common/subject-uuid">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/select-subject-by-id/type" class="toc2 name">type</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/select-subject-by-id/type">Switch to XML</a></div>
                     <p class="formal-name">Subject Universally Unique Identifier Reference Type</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">type</code></p>
                     <p class="definition-link"><a href="#/flag/oscal-assessment-common/subject-type">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/select-subject-by-id/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/select-subject-by-id/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/select-subject-by-id/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/select-subject-by-id/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/select-subject-by-id/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/select-subject-by-id/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-implementation-common/set-parameter" class="toc1 name">set-parameter</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/set-parameter">Switch to XML</a></div>
         <p class="formal-name">Set Parameter Value</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Identifies the parameter that will be set by the enclosed value.</p>
         <details open="open">
            <summary>Properties (3)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/set-parameter/param-id" class="toc2 name">param-id</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/set-parameter/param-id">Switch to XML</a></div>
                     <p class="formal-name">Parameter ID</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/flag/oscal-implementation-common/param-id">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/set-parameter/values" class="toc2 name">value</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[1 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/set-parameter/value">Switch to XML</a></div>
                     <p class="formal-name">Parameter Value</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A parameter value or set of values.</p>
                     <p><span class="usa-tag">use name</span> <code class="name">value</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">values</code></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/set-parameter/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/set-parameter/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-flag">
      <div class="definition-header">
         <h1 id="/flag/oscal-implementation-common/source" class="toc1 name">source</h1>
         <p class="type"><a href="/reference/datatypes/#uri-reference">uri-reference</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/flag/oscal-implementation-common/source">Switch to XML</a></div>
         <p class="formal-name">Source Resource Reference</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A reference to an OSCAL catalog or profile providing the referenced control or subcontrol
            definition.</p>
      </div>
   </div>
   <div class="model-entry definition define-flag">
      <div class="definition-header">
         <h1 id="/flag/oscal-implementation-common/statement-id" class="toc1 name">statement-id</h1>
         <p class="type"><a href="/reference/datatypes/#token">token</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/flag/oscal-implementation-common/statement-id">Switch to XML</a></div>
         <p class="formal-name">Control Statement Reference</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#human-oriented">human-oriented</a> identifier reference to a <code>control statement</code>.</p>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-assessment-common/subject-reference" class="toc1 name">subject-reference</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/subject-reference">Switch to XML</a></div>
         <p class="formal-name">Identifies the Subject</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#human-oriented">human-oriented</a> identifier reference to a resource. Use type to indicate whether the identified resource
            is a component, inventory item, location, user, or something else.</p>
         <div class="remarks-group usa-prose">
            <details open="open">
               <summary class="subhead">Remarks</summary>
               <div class="remarks">
                  <p>The subject reference UUID could point to an item defined in the SSP, AP, or AR.</p>
                  <p>Tools should check look for the ID in every file imported directly or indirectly.</p>
               </div>
            </details>
         </div>
         <details open="open">
            <summary>Properties (6)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/subject-reference/subject-uuid" class="toc2 name">subject-uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/subject-reference/subject-uuid">Switch to XML</a></div>
                     <p class="formal-name">Subject Universally Unique Identifier Reference</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/flag/oscal-assessment-common/subject-uuid">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/subject-reference/type" class="toc2 name">type</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/subject-reference/type">Switch to XML</a></div>
                     <p class="formal-name">Subject Universally Unique Identifier Reference Type</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">type</code></p>
                     <p class="definition-link"><a href="#/flag/oscal-assessment-common/subject-type">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/subject-reference/title" class="toc2 name">title</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/subject-reference/title">Switch to XML</a></div>
                     <p class="formal-name">Subject Reference Title</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> The title or name for the referenced subject.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/subject-reference/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/subject-reference/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/subject-reference/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/subject-reference/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/subject-reference/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/subject-reference/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-flag">
      <div class="definition-header">
         <h1 id="/flag/oscal-assessment-common/subject-type" class="toc1 name">subject-type</h1>
         <p class="type"><a href="/reference/datatypes/#token">token</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/flag/oscal-assessment-common/subject-type">Switch to XML</a></div>
         <p class="formal-name">Subject Universally Unique Identifier Reference Type</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Used to indicate the type of object pointed to by the <code>uuid-ref</code> within a subject.</p>
         <details>
            <summary>Constraint (1)</summary>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span></p>
               <p>The value <b>may be locally defined</b>, or one of the following:</p>
               <ul>
                  
                  <li><strong>component</strong>: Component</li>
                  
                  <li><strong>inventory-item</strong>: Inventory Item</li>
                  
                  <li><strong>location</strong>: Location</li>
                  
                  <li><strong>party</strong>: Interview Party</li>
                  
                  <li><strong>user</strong>: User</li>
                  
                  <li><strong>resource</strong>: Resource or Artifact</li>
                  </ul>
            </div>
            </details>
      </div>
   </div>
   <div class="model-entry definition define-flag">
      <div class="definition-header">
         <h1 id="/flag/oscal-assessment-common/subject-uuid" class="toc1 name">subject-uuid</h1>
         <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/flag/oscal-assessment-common/subject-uuid">Switch to XML</a></div>
         <p class="formal-name">Subject Universally Unique Identifier Reference</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a> identifier reference to a component, inventory-item, location, party, user, or resource
            using it's UUID.</p>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-implementation-common/system-component" class="toc1 name">system-component</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/system-component">Switch to XML</a></div>
         <p class="formal-name">Component</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A defined component that can be part of an implemented system.</p>
         <div class="remarks-group usa-prose">
            <details open="open">
               <summary class="subhead">Remarks</summary>
               <div class="remarks">
                  <p>Components may be products, services, application programming interface (APIs), policies,
                     processes, plans, guidance, standards, or other tangible items that enable security
                     and/or privacy.</p>
                  <p>The <code>type</code> indicates which of these component types is represented.</p>
                  <p>When defining a <code>service</code> component where are relationship to other components is known, one or more <code>link</code> entries with rel values of provided-by and used-by can be used to link to the specific
                     component identifier(s) that provide and use the service respectively.</p>
               </div>
            </details>
         </div>
         <details>
            <summary>Constraints (24)</summary>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">prop/@name</code></p>
               <p>The value <b>may be locally defined</b>, or one of the following:</p>
               <ul>
                  
                  
                  <li><strong>implementation-point</strong>: Relative placement of component ('internal' or 'external') to the system.</li>
                  
                  <li><strong>leveraged-authorization-uuid</strong>: UUID of the related leveraged-authorization assembly in this SSP.</li>
                  
                  <li><strong>inherited-uuid</strong>: UUID of the component as it was assigned in the leveraged system's SSP.</li>
                  
                  
                  
                  
                  
                  
                  
                  <li><strong>asset-type</strong>: Simple indication of the asset's function, such as Router, Storage Array, DNS Server.</li>
                  
                  <li><strong>asset-id</strong>: An organizationally specific identifier that is used to uniquely identify a logical
                     or tangible item by the organization that owns the item.</li>
                  
                  <li><strong>asset-tag</strong>: An asset tag assigned by the organization responsible for maintaining the logical
                     or tangible item.</li>
                  
                  <li><strong>public</strong>: Identifies whether the asset is publicly accessible (yes/no)</li>
                  
                  <li><strong>virtual</strong>: Identifies whether the asset is virtualized (yes/no)</li>
                  
                  <li><strong>vlan-id</strong>: Virtual LAN identifier of the asset.</li>
                  
                  <li><strong>network-id</strong>: The network identifier of the asset.</li>
                  
                  <li><strong>label</strong>: A human-readable label for the parent context.</li>
                  
                  <li><strong>sort-id</strong>: An alternative identifier, whose value is easily sortable among other such values
                     in the document.</li>
                  
                  <li><strong>baseline-configuration-name</strong>: The name of the baseline configuration for the asset.</li>
                  
                  <li><strong>allows-authenticated-scan</strong>: Can the asset be check with an authenticated scan? (yes/no)</li>
                  
                  <li><strong>function</strong>: The function provided by the asset for the system.</li>
                  
                  
                  
                  
                  <li><strong>version</strong>: The version of the component.</li>
                  
                  <li><strong>patch-level</strong>: The specific patch level of the component.</li>
                  
                  <li><strong>model</strong>: The model of the component.</li>
                  
                  
                  <li><strong>release-date</strong>: The date the component was released, such as a software release date or policy publication
                     date.</li>
                  
                  <li><strong>validation-type</strong>: Used with component-type='validation' to provide a well-known name for a kind of
                     validation.</li>
                  
                  <li><strong>validation-reference</strong>: Used with component-type='validation' to indicate the validating body's assigned
                     identifier for their validation of this component.</li>
                  
                  </ul>
            </div>
            
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">link/@rel</code></p>
               <p>The value <b>may be locally defined</b>, or one of the following:</p>
               <ul>
                  
                  
                  
                  
                  
                  <li><strong>depends-on</strong>: A reference to another component that this component has a dependency on.</li>
                  
                  
                  <li><strong>validation</strong>: A reference to another component of component-type=validation, that is a validation
                     (e.g., FIPS 140-2) for this component</li>
                  
                  <li><strong>proof-of-compliance</strong>: A pointer to a validation record (e.g., FIPS 140-2) or other compliance information.</li>
                  
                  
                  <li><strong>baseline-template</strong>: A reference to the baseline template used to configure the asset.</li>
                  
                  <li><strong>uses-service</strong>: This service is used by the referenced component identifier.</li>
                  
                  <li><strong>system-security-plan</strong>: A link to the system security plan of the external system.</li>
                  
                  
                  <li><strong>uses-network</strong>: This component uses the network provided by the identified network component.</li>
                  </ul>
            </div>
            
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">responsible-role/@role-id</code></p>
               <p>The value <b>may be locally defined</b>, or one of the following:</p>
               <ul>
                  
                  
                  
                  
                  <li><strong>asset-owner</strong>: Accountable for ensuring the asset is managed in accordance with organizational
                     policies and procedures.</li>
                  
                  <li><strong>asset-administrator</strong>: Responsible for administering a set of assets.</li>
                  
                  
                  <li><strong>security-operations</strong>: Members of the security operations center (SOC).</li>
                  
                  
                  <li><strong>network-operations</strong>: Members of the network operations center (NOC).</li>
                  
                  <li><strong>incident-response</strong>: Responsible for responding to an event that could lead to loss of, or disruption
                     to, an organization's operations, services or functions.</li>
                  
                  <li><strong>help-desk</strong>: Responsible for providing information and support to users.</li>
                  
                  
                  <li><strong>configuration-management</strong>: Responsible for the configuration management processes governing changes to the
                     asset.</li>
                  
                  
                  <li><strong>maintainer</strong>: Responsible for the creation and maintenance of a component.</li>
                  
                  <li><strong>provider</strong>: Organization responsible for providing the component, if this is different from
                     the "maintainer" (e.g., a reseller).</li>
                  
                  </ul>
            </div>
            
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">prop[@name='asset-type']/@value</code></p>
               <p>The value <b>must</b> be one of the following:</p>
               <ul>
                  
                  
                  
                  <li><strong>operating-system</strong>: System software that manages computer hardware, software resources, and provides
                     common services for computer programs.</li>
                  
                  <li><strong>database</strong>: An electronic collection of data, or information, that is specially organized for
                     rapid search and retrieval.</li>
                  
                  <li><strong>web-server</strong>: A system that delivers content or services to end users over the Internet or an
                     intranet.</li>
                  
                  <li><strong>dns-server</strong>: A system that resolves domain names to internet protocol (IP) addresses.</li>
                  
                  <li><strong>email-server</strong>: A computer system that sends and receives electronic mail messages.</li>
                  
                  <li><strong>directory-server</strong>: A  system that stores, organizes and provides access to directory information in
                     order to unify network resources.</li>
                  
                  <li><strong>pbx</strong>: A private branch exchange (PBX) provides a a private telephone switchboard.</li>
                  
                  <li><strong>firewall</strong>: A network security system that monitors and controls incoming and outgoing network
                     traffic based on predetermined security rules.</li>
                  
                  <li><strong>router</strong>: A physical or virtual networking device that forwards data packets between computer
                     networks.</li>
                  
                  <li><strong>switch</strong>: A physical or virtual networking device that connects devices within a computer
                     network by using packet switching to receive and forward data to the destination device.</li>
                  
                  <li><strong>storage-array</strong>: A consolidated, block-level data storage capability.</li>
                  
                  <li><strong>appliance</strong>: A physical or virtual machine that centralizes hardware, software, or services for
                     a specific purpose.</li>
                  
                  </ul>
            </div>
            
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">prop[@name='allows-authenticated-scan']/@value</code></p>
               <p>The value <b>must</b> be one of the following:</p>
               <ul>
                  
                  <li><strong>yes</strong>: The component allows an authenticated scan.</li>
                  
                  <li><strong>no</strong>: The component does not allow an authenticated scan.</li>
                  </ul>
            </div>
            
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">prop[@name='public']/@value</code></p>
               <p>The value <b>must</b> be one of the following:</p>
               <ul>
                  
                  <li><strong>yes</strong>: The component is publicly accessible.</li>
                  
                  <li><strong>no</strong>: The component is not publicly accessible.</li>
                  </ul>
            </div>
            
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">prop[@name='virtual']/@value</code></p>
               <p>The value <b>must</b> be one of the following:</p>
               <ul>
                  
                  <li><strong>yes</strong>: The component is virtualized.</li>
                  
                  <li><strong>no</strong>: The component is not virtualized.</li>
                  </ul>
            </div>
            
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">prop[@name='implementation-point']/@value</code></p>
               <p>The value <b>must</b> be one of the following:</p>
               <ul>
                  
                  <li><strong>internal</strong>: The component is implemented within the system boundary.</li>
                  
                  <li><strong>external</strong>: The component is implemented outside the system boundary.</li>
                  </ul>
            </div>
            
            
            <div class="constraint">
               <p><span class="usa-tag">index has key</span> for <code class="path">prop[@name='physical-location']</code>this value must correspond to a listing in the index <code>index-metadata-location-uuid</code> using a key constructed of key field(s) <code>@value</code></p>
            </div>
            
            
            <div class="constraint">
               <p><span class="usa-tag">matches</span> for <code class="path">prop[@name='inherited-uuid']/@value</code>: the target value must match the lexical form of the 'uuid' data type.</p>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">matches</span> for <code class="path">prop[@name='release-date']/@value</code>: the target value must match the lexical form of the 'date' data type.</p>
            </div>
            
            
            
            
            
            
            <div class="constraint">
               <p><span class="usa-tag">allowed value</span> for <code class="path">(.)[@type=('software', 'hardware', 'service')]/prop/@name</code></p>
               <p>The value <b>may be locally defined</b>, or the following:</p>
               <ul>
                  
                  <li><strong>vendor-name</strong>: The name of the company or organization </li>
                  </ul>
            </div>
            
            
            
            
            
            
            
            
            <div class="constraint">
               <p><span class="usa-tag">allowed value</span> for <code class="path">(.)[@type='validation']/link/@rel</code></p>
               <p>The value <b>may be locally defined</b>, or the following:</p>
               <ul>
                  
                  <li><strong>validation-details</strong>: A link to an online information provided by the authorizing body.</li>
                  </ul>
            </div>
            
            
            
            
            
            <div class="constraint">
               <p><span class="usa-tag">allowed value</span> for <code class="path">(.)[@type='software']/prop/@name</code></p>
               <p>The value <b>may be locally defined</b>, or the following:</p>
               <ul>
                  
                  <li><strong>software-identifier</strong>: If a "software" component-type, the identifier, such as a SWID tag, for the software
                     component.</li>
                  
                  </ul>
            </div>
            
            
            
            
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@type='service']/link/@rel</code></p>
               <p>The value <b>may be locally defined</b>, or one of the following:</p>
               <ul>
                  
                  <li><strong>provided-by</strong>: This service is provided by the referenced component identifier.</li>
                  
                  
                  <li><strong>used-by</strong>: This service is used by the referenced component identifier.</li>
                  
                  </ul>
            </div>
            
            
            
            
            
            
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@type='interconnection']/prop/@name</code></p>
               <p>The value <b>may be locally defined</b>, or one of the following:</p>
               <ul>
                  
                  <li><strong>isa-title</strong>: Title of the Interconnection Security Agreement (ISA).</li>
                  
                  <li><strong>isa-date</strong>: Date of the Interconnection Security Agreement (ISA).</li>
                  
                  <li><strong>isa-remote-system-name</strong>: The name of the remote interconnected system.</li>
                  
                  <li><strong>ipv4-address</strong>: An Internet Protocol Version 4 interconnection address</li>
                  
                  <li><strong>ipv6-address</strong>: An Internet Protocol Version 6 interconnection address</li>
                  
                  <li><strong>direction</strong>: An Internet Protocol Version 6 interconnection address</li>
                  </ul>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">prop[@name=('ipv4-address','ipv6-address')]/@class</code></p>
               <p>The value <b>may be locally defined</b>, or one of the following:</p>
               <ul>
                  
                  <li><strong>local</strong>: The identified IP address is for this system.</li>
                  
                  <li><strong>remote</strong>: The identified IP address is for the remote system to which this system is connected.</li>
                  </ul>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed value</span> for <code class="path">(.)[@type='interconnection']/link/@rel</code></p>
               <p>The value <b>may be locally defined</b>, or the following:</p>
               <ul>
                  
                  
                  <li><strong>isa-agreement</strong>: A link to the system interconnection agreement.</li>
                  </ul>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">(.)[@type='interconnection']/responsible-role/@role-id</code></p>
               <p>The value <b>may be locally defined</b>, or one of the following:</p>
               <ul>
                  
                  <li><strong>isa-poc-local</strong>: Interconnection Security Agreement (ISA) point of contact (POC) for this system.</li>
                  
                  <li><strong>isa-poc-remote</strong>: Interconnection Security Agreement (ISA) point of contact (POC) for the remote interconnected
                     system.</li>
                  
                  <li><strong>isa-authorizing-official-local</strong>: Interconnection Security Agreement (ISA) authorizing official for this system.</li>
                  
                  <li><strong>isa-authorizing-official-remote</strong>: Interconnection Security Agreement (ISA) authorizing official for the remote interconnected
                     system.</li>
                  </ul>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">matches</span> for <code class="path">prop[@name='isa-date']/@value</code>: the target value must match the lexical form of the 'dateTime' data type.</p>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">matches</span> for <code class="path">prop[@name='ipv4-address']/@value</code>: the target value must match the lexical form of the 'ip-v4-address' data type.</p>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">matches</span> for <code class="path">prop[@name='ipv6-address']/@value</code>: the target value must match the lexical form of the 'ip-v6-address' data type.</p>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">prop[@name='direction']/@value</code></p>
               <p>The value <b>may be locally defined</b>, or one of the following:</p>
               <ul>
                  
                  <li><strong>incoming</strong>: Data from the remote system flows into this system.</li>
                  
                  <li><strong>outgoing</strong>: Data from this system flows to the remote system.</li>
                  </ul>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">is unique</span> for <code class="path">responsible-role</code>: any target value must be unique (i.e., occur only once)</p>
            </div>
            </details>
         <details open="open">
            <summary>Properties (11)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/system-component/uuid" class="toc2 name">uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/system-component/uuid">Switch to XML</a></div>
                     <p class="formal-name">Component Identifier</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this component elsewhere in <a href="/concepts/identifier-use/#scope">this or other OSCAL instances</a>. The locally defined <em>UUID</em> of the <code>component</code> can be used to reference the data item locally or globally (e.g., in an imported
                        OSCAL instance). This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                        of the document.</p>
                  </div>
               </div>
               <div class="model-entry definition flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/system-component/type" class="toc2 name">type</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/system-component/type">Switch to XML</a></div>
                     <p class="formal-name">Component Type</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">type</code></p>
                     <p class="definition-link"><a href="#/flag/oscal-implementation-common/system-component-type">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/system-component/title" class="toc2 name">title</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/system-component/title">Switch to XML</a></div>
                     <p class="formal-name">Component Title</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A human readable name for the system component.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/system-component/description" class="toc2 name">description</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/system-component/description">Switch to XML</a></div>
                     <p class="formal-name">Component Description</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A description of the component, including information about its function.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/system-component/purpose" class="toc2 name">purpose</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/system-component/purpose">Switch to XML</a></div>
                     <p class="formal-name">Purpose</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A summary of the technological or business purpose of the component.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/system-component/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/system-component/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/system-component/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/system-component/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/system-component/status" class="toc2 name">status</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/system-component/status">Switch to XML</a></div>
                     <p class="formal-name">Status</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Describes the operational status of the system component.</p>
                     <details open="open">
                        <summary>Properties (2)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition define-flag">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-implementation-common/system-component/status/state" class="toc3 name">state</h3>
                                 <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/system-component/status/state">Switch to XML</a></div>
                                 <p class="formal-name">State</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> The operational status.</p>
                                 <details>
                                    <summary>Constraint (1)</summary>
                                    
                                    <div class="constraint">
                                       <p><span class="usa-tag">allowed values</span></p>
                                       <p>The value <b>must</b> be one of the following:</p>
                                       <ul>
                                          
                                          <li><strong>under-development</strong>: The component is being designed, developed, or implemented.</li>
                                          
                                          <li><strong>operational</strong>: The component is currently operational and is available for use in the system.</li>
                                          
                                          <li><strong>disposition</strong>: The component is no longer operational.</li>
                                          
                                          <li><strong>other</strong>: Some other state.</li>
                                          </ul>
                                    </div>
                                    </details>
                              </div>
                           </div>
                           <div class="model-entry definition field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-implementation-common/system-component/status/remarks" class="toc3 name">remarks</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/system-component/status/remarks">Switch to XML</a></div>
                                 <p class="formal-name">Remarks</p>
                              </div>
                              <div class="body">
                                 <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/system-component/responsible-roles" class="toc2 name">responsible-role</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/system-component/responsible-role">Switch to XML</a></div>
                     <p class="formal-name">Responsible Role</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">responsible-roles</code></p>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/responsible-role">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/system-component/protocols" class="toc2 name">protocol</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/system-component/protocol">Switch to XML</a></div>
                     <p class="formal-name">Service Protocol Information</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">protocols</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Used for <code>service</code> components to define the protocols supported by the service.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-implementation-common/protocol">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/system-component/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/system-component/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-flag">
      <div class="definition-header">
         <h1 id="/flag/oscal-implementation-common/system-component-type" class="toc1 name">system-component-type</h1>
         <p class="type"><a href="/reference/datatypes/#string">string</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/flag/oscal-implementation-common/system-component-type">Switch to XML</a></div>
         <p class="formal-name">Component Type</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A category describing the purpose of the component.</p>
         <details>
            <summary>Constraint (1)</summary>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span></p>
               <p>The value <b>may be locally defined</b>, or one of the following:</p>
               <ul>
                  
                  <li><strong>this-system</strong>: The system as a whole.</li>
                  
                  <li><strong>system</strong>: An external system, which may be a leveraged system or the other side of an interconnection.</li>
                  
                  <li><strong>interconnection</strong>: A connection to something outside this system.</li>
                  
                  <li><strong>software</strong>: Any software, operating system, or firmware.</li>
                  
                  <li><strong>hardware</strong>: A physical device.</li>
                  
                  <li><strong>service</strong>: A service that may provide APIs.</li>
                  
                  <li><strong>policy</strong>: An enforceable policy.</li>
                  
                  <li><strong>physical</strong>: A tangible asset used to provide physical protections or countermeasures.</li>
                  
                  
                  <li><strong>process-procedure</strong>: A list of steps or actions to take to achieve some end result.</li>
                  
                  <li><strong>plan</strong>: An applicable plan.</li>
                  
                  <li><strong>guidance</strong>: Any guideline or recommendation.</li>
                  
                  <li><strong>standard</strong>: Any organizational or industry standard.</li>
                  
                  <li><strong>validation</strong>: An external assessment performed on some other component, that has been validated
                     by a third-party.</li>
                  
                  
                  <li><strong>network</strong>: A physical or virtual network.</li>
                  </ul>
            </div>
            </details>
      </div>
   </div>
   <div class="model-entry definition define-field">
      <div class="definition-header">
         <h1 id="/field/oscal-implementation-common/system-id" class="toc1 name">system-id</h1>
         <p class="type"><a href="/reference/datatypes/#string">string</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-implementation-common/system-id">Switch to XML</a></div>
         <p class="formal-name">System Identification</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#human-oriented">human-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this system identification property elsewhere
            in <a href="/concepts/identifier-use/#scope">this or other OSCAL instances</a>. When referencing an externally defined <code>system identification</code>, the <code>system identification</code> must be used in the context of the external / imported OSCAL instance (e.g., uri-reference).
            This string should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same system across revisions
            of the document.</p>
         <p><span class="usa-tag">value key</span> <code class="name">id</code></p>
         <details open="open">
            <summary>Properties (2)</summary>
            <div class="model field-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/field/oscal-implementation-common/system-id/identifier-type" class="toc2 name">identifier-type</h2>
                     <p class="type"><a href="/reference/datatypes/#uri">uri</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-implementation-common/system-id/identifier-type">Switch to XML</a></div>
                     <p class="formal-name">Identification System Type</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Identifies the identification system from which the provided identifier was assigned.
                        </p>
                     <details>
                        <summary>Constraint (1)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span></p>
                           <p>The value <b>may be locally defined</b>, or one of the following:</p>
                           <ul>
                              
                              <li><strong>https://fedramp.gov</strong>: The identifier was assigned by FedRAMP.</li>
                              
                              <li><strong>https://ietf.org/rfc/rfc4122</strong>: A Universally Unique Identifier (UUID) as defined by RFC4122.</li>
                              </ul>
                        </div>
                        </details>
                  </div>
               </div>
               <div class="model-entry definition m:define-flag">
                  <div class="instance-header">
                     <h2 id="/field/oscal-implementation-common/system-id/id" class="toc2 name">id</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-implementation-common/system-id">Switch to XML</a></div>
                     <p class="formal-name">System Identification Value</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> This property provides the (nominal) value for this object as a whole.</p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-implementation-common/system-user" class="toc1 name">system-user</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/system-user">Switch to XML</a></div>
         <p class="formal-name">System User</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A type of user that interacts with the system based on an associated role.</p>
         <div class="remarks-group usa-prose">
            <details open="open">
               <summary class="subhead">Remarks</summary>
               <div class="remarks">
                  <p>Permissible values to be determined closer to the application, such as by a receiving
                     authority.</p>
               </div>
            </details>
         </div>
         <details>
            <summary>Constraints (4)</summary>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">prop/@name</code></p>
               <p>The value <b>may be locally defined</b>, or one of the following:</p>
               <ul>
                  
                  <li><strong>type</strong>: The type of user, such as internal, external, or general-public.</li>
                  
                  <li><strong>privilege-level</strong>: The user's privilege level within the system, such as privileged, non-privileged,
                     no-logical-access.</li>
                  </ul>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">prop[@name='type']/@value</code></p>
               <p>The value <b>must</b> be one of the following:</p>
               <ul>
                  
                  <li><strong>internal</strong>: A user account for a person or entity that is part of the organization who owns
                     or operates the system.</li>
                  
                  <li><strong>external</strong>: A user account for a person or entity that is not part of the organization who owns
                     or operates the system.</li>
                  
                  <li><strong>general-public</strong>: A user of the system considered to be outside </li>
                  </ul>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">prop[@name='privilege-level']/@value</code></p>
               <p>The value <b>must</b> be one of the following:</p>
               <ul>
                  
                  <li><strong>privileged</strong>: This role has elevated access to the system, such as a group or system administrator.</li>
                  
                  <li><strong>non-privileged</strong>: This role has typical user-level access to the system without elevated access.</li>
                  
                  <li><strong>no-logical-access</strong>: This role has no access to the system, such as a manager who approves access as
                     part of a process.</li>
                  </ul>
            </div>
            
            <div class="constraint">
               <p><span class="usa-tag">allowed values</span> for <code class="path">role-id</code></p>
               <p>The value <b>may be locally defined</b>, or one of the following:</p>
               <ul>
                  
                  <li><strong>asset-owner</strong>: Accountable for ensuring the asset is managed in accordance with organizational
                     policies and procedures.</li>
                  
                  <li><strong>asset-administrator</strong>: Responsible for administering a set of assets.</li>
                  
                  
                  <li><strong>security-operations</strong>: Members of the security operations center (SOC).</li>
                  
                  
                  <li><strong>network-operations</strong>: Members of the network operations center (NOC).</li>
                  
                  <li><strong>incident-response</strong>: Responsible for responding to an event that could lead to loss of, or disruption
                     to, an organization's operations, services or functions.</li>
                  
                  <li><strong>help-desk</strong>: Responsible for providing information and support to users.</li>
                  
                  
                  <li><strong>configuration-management</strong>: Responsible for the configuration management processes governing changes to the
                     asset.</li>
                  
                  </ul>
            </div>
            </details>
         <details open="open">
            <summary>Properties (9)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/system-user/uuid" class="toc2 name">uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/system-user/uuid">Switch to XML</a></div>
                     <p class="formal-name">User Universally Unique Identifier</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this user class elsewhere in <a href="/concepts/identifier-use/#scope">this or other OSCAL instances</a>. The locally defined <em>UUID</em> of the <code>system user</code> can be used to reference the data item locally or globally (e.g., in an imported
                        OSCAL instance). This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                        of the document.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/system-user/title" class="toc2 name">title</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/system-user/title">Switch to XML</a></div>
                     <p class="formal-name">User Title</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A name given to the user, which may be used by a tool for display and navigation.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/system-user/short-name" class="toc2 name">short-name</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/system-user/short-name">Switch to XML</a></div>
                     <p class="formal-name">User Short Name</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A short common name, abbreviation, or acronym for the user.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/system-user/description" class="toc2 name">description</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/system-user/description">Switch to XML</a></div>
                     <p class="formal-name">User Description</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A summary of the user's purpose within the system.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/system-user/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/system-user/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/system-user/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/system-user/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/system-user/role-ids" class="toc2 name">role-id</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/system-user/role-id">Switch to XML</a></div>
                     <p class="formal-name">Role Identifier Reference</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">role-ids</code></p>
                     <p class="definition-link"><a href="#/field/oscal-metadata/role-id">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/system-user/authorized-privileges" class="toc2 name">authorized-privilege</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/system-user/authorized-privilege">Switch to XML</a></div>
                     <p class="formal-name">Privilege</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">authorized-privileges</code></p>
                     <p class="definition-link"><a href="#/assembly/oscal-implementation-common/authorized-privilege">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-implementation-common/system-user/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-implementation-common/system-user/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-assembly">
      <div class="definition-header">
         <h1 id="/assembly/oscal-assessment-common/task" class="toc1 name">task</h1>
         <p class="type">assembly<br class="br" /> </p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task">Switch to XML</a></div>
         <p class="formal-name">Task</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Represents a scheduled event or milestone, which may be associated with a series
            of assessment actions.</p>
         <details open="open">
            <summary>Properties (13)</summary>
            <div class="model assembly-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/task/uuid" class="toc2 name">uuid</h2>
                     <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/uuid">Switch to XML</a></div>
                     <p class="formal-name">Task Universally Unique Identifier</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a>, <a href="/concepts/identifier-use/#globally-unique">globally unique</a> identifier with <a href="/concepts/identifier-use/#cross-instance">cross-instance</a> scope that can be used to reference this task elsewhere in <a href="/concepts/identifier-use/#scope">this or other OSCAL instances</a>. The locally defined <em>UUID</em> of the <code>task</code> can be used to reference the data item locally or globally (e.g., in an imported
                        OSCAL instance). This UUID should be assigned <a href="/concepts/identifier-use/#consistency">per-subject</a>, which means it should be consistently used to identify the same subject across revisions
                        of the document.</p>
                  </div>
               </div>
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/task/type" class="toc2 name">type</h2>
                     <p class="type"><a href="/reference/datatypes/#token">token</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/type">Switch to XML</a></div>
                     <p class="formal-name">Task Type</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> The type of task.</p>
                     <details>
                        <summary>Constraint (1)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span></p>
                           <p>The value <b>may be locally defined</b>, or one of the following:</p>
                           <ul>
                              
                              <li><strong>milestone</strong>: The task represents a planned milestone.</li>
                              
                              <li><strong>action</strong>: The task represents a specific assessment action to be performed.</li>
                              </ul>
                        </div>
                        </details>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/task/title" class="toc2 name">title</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-line">markup-line</a></p>
                     <p class="occurrence">[1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/title">Switch to XML</a></div>
                     <p class="formal-name">Task Title</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> The title for this task.</p>
                  </div>
               </div>
               <div class="model-entry definition define-field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/task/description" class="toc2 name">description</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/description">Switch to XML</a></div>
                     <p class="formal-name">Task Description</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> A human-readable description of this task.</p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/task/props" class="toc2 name">property</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/prop">Switch to XML</a></div>
                     <p class="formal-name">Property</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Properties permit the deployment and management of arbitrary controlled values, within
                                 OSCAL objects. A property can be included for any purpose useful to an application
                                 or implementation. Typically, properties will be used to sort, filter, select, order,
                                 and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                 an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                 lexical composition of properties may be constrained by external processes to ensure
                                 consistency.</p>
                              <p>Property allows for associated remarks that describe why the specific property value
                                 was applied to the containing object, or the significance of the value in the context
                                 of the containing object.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/task/links" class="toc2 name">link</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/link">Switch to XML</a></div>
                     <p class="formal-name">Link</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                 a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                              <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/task/timing" class="toc2 name">timing</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/timing">Switch to XML</a></div>
                     <p class="formal-name">Event Timing</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> The timing under which the task is intended to occur.</p>
                     <details open="open">
                        <summary>Property (1)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition define-assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/task/timing/on-date" class="toc3 name">on-date</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/timing/on-date">Switch to XML</a></div>
                                 <p class="formal-name">On Date Condition</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> The task is intended to occur on the specified date.</p>
                                 <details open="open">
                                    <summary>Property (1)</summary>
                                    <div class="model assembly-model">
                                       <div class="model-entry definition define-flag">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-assessment-common/task/timing/on-date/date" class="toc4 name">date</h4>
                                             <p class="type"><a href="/reference/datatypes/#datetime-with-timezone">dateTime-with-timezone</a></p>
                                             <p class="occurrence">[0 or 1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/timing/on-date/date">Switch to XML</a></div>
                                             <p class="formal-name">On Date Condition</p>
                                          </div>
                                          <div class="body">
                                             <p class="description"><span class="usa-tag">description</span> The task must occur on the specified date.</p>
                                          </div>
                                       </div>
                                    </div>
                                 </details>
                              </div>
                           </div>
                           <div class="model-entry definition define-assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/task/timing/within-date-range" class="toc3 name">within-date-range</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/timing/within-date-range">Switch to XML</a></div>
                                 <p class="formal-name">On Date Range Condition</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> The task is intended to occur within the specified date range.</p>
                                 <details open="open">
                                    <summary>Properties (2)</summary>
                                    <div class="model assembly-model">
                                       <div class="model-entry definition define-flag">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-assessment-common/task/timing/within-date-range/start" class="toc4 name">start</h4>
                                             <p class="type"><a href="/reference/datatypes/#datetime-with-timezone">dateTime-with-timezone</a></p>
                                             <p class="occurrence">[0 or 1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/timing/within-date-range/start">Switch to XML</a></div>
                                             <p class="formal-name">Start Date Condition</p>
                                          </div>
                                          <div class="body">
                                             <p class="description"><span class="usa-tag">description</span> The task must occur on or after the specified date.</p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition define-flag">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-assessment-common/task/timing/within-date-range/end" class="toc4 name">end</h4>
                                             <p class="type"><a href="/reference/datatypes/#datetime-with-timezone">dateTime-with-timezone</a></p>
                                             <p class="occurrence">[0 or 1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/timing/within-date-range/end">Switch to XML</a></div>
                                             <p class="formal-name">End Date Condition</p>
                                          </div>
                                          <div class="body">
                                             <p class="description"><span class="usa-tag">description</span> The task must occur on or before the specified date.</p>
                                          </div>
                                       </div>
                                    </div>
                                 </details>
                              </div>
                           </div>
                           <div class="model-entry definition define-assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/task/timing/at-frequency" class="toc3 name">at-frequency</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/timing/at-frequency">Switch to XML</a></div>
                                 <p class="formal-name">Frequency Condition</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> The task is intended to occur at the specified frequency.</p>
                                 <details open="open">
                                    <summary>Properties (2)</summary>
                                    <div class="model assembly-model">
                                       <div class="model-entry definition define-flag">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-assessment-common/task/timing/at-frequency/period" class="toc4 name">period</h4>
                                             <p class="type"><a href="/reference/datatypes/#positiveinteger">positiveInteger</a></p>
                                             <p class="occurrence">[0 or 1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/timing/at-frequency/period">Switch to XML</a></div>
                                             <p class="formal-name">Period</p>
                                          </div>
                                          <div class="body">
                                             <p class="description"><span class="usa-tag">description</span> The task must occur after the specified period has elapsed.</p>
                                          </div>
                                       </div>
                                       <div class="model-entry definition define-flag">
                                          <div class="instance-header">
                                             <h4 id="/assembly/oscal-assessment-common/task/timing/at-frequency/unit" class="toc4 name">unit</h4>
                                             <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                                             <p class="occurrence">[0 or 1]</p>
                                             <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/timing/at-frequency/unit">Switch to XML</a></div>
                                             <p class="formal-name">Time Unit</p>
                                          </div>
                                          <div class="body">
                                             <p class="description"><span class="usa-tag">description</span> The unit of time for the period.</p>
                                             <details>
                                                <summary>Constraint (1)</summary>
                                                
                                                <div class="constraint">
                                                   <p><span class="usa-tag">allowed values</span></p>
                                                   <p>The value <b>must</b> be one of the following:</p>
                                                   <ul>
                                                      
                                                      <li><strong>seconds</strong>: The period is specified in seconds.</li>
                                                      
                                                      <li><strong>minutes</strong>: The period is specified in minutes.</li>
                                                      
                                                      <li><strong>hours</strong>: The period is specified in hours.</li>
                                                      
                                                      <li><strong>days</strong>: The period is specified in days.</li>
                                                      
                                                      <li><strong>months</strong>: The period is specified in calendar months.</li>
                                                      
                                                      <li><strong>years</strong>: The period is specified in calendar years.</li>
                                                      </ul>
                                                </div>
                                                </details>
                                          </div>
                                       </div>
                                    </div>
                                 </details>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/task/dependencies" class="toc2 name">dependency</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/dependency">Switch to XML</a></div>
                     <p class="formal-name">Task Dependency</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Used to indicate that a task is dependent on another task.</p>
                     <p><span class="usa-tag">group as</span> <code class="name">dependencies</code></p>
                     <details open="open">
                        <summary>Properties (2)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition define-flag">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/task/dependencies/task-uuid" class="toc3 name">task-uuid</h3>
                                 <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/dependency/task-uuid">Switch to XML</a></div>
                                 <p class="formal-name">Task Universally Unique Identifier Reference</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a> identifier reference to a unique task.</p>
                              </div>
                           </div>
                           <div class="model-entry definition field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/task/dependencies/remarks" class="toc3 name">remarks</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/dependency/remarks">Switch to XML</a></div>
                                 <p class="formal-name">Remarks</p>
                              </div>
                              <div class="body">
                                 <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/task/tasks" class="toc2 name">task</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/task">Switch to XML</a></div>
                     <p class="formal-name">Task</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">tasks</code></p>
                     <p class="definition-link"><a href="#/assembly/oscal-assessment-common/task">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition define-assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/task/associated-activities" class="toc2 name">associated-activity</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/associated-activity">Switch to XML</a></div>
                     <p class="formal-name">Associated Activity</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Identifies an individual activity to be performed as part of a task.</p>
                     <p><span class="usa-tag">group as</span> <code class="name">associated-activities</code></p>
                     <details>
                        <summary>Constraint (1)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">is unique</span> for <code class="path">responsible-role</code>: any target value must be unique (i.e., occur only once)</p>
                        </div>
                        </details>
                     <details open="open">
                        <summary>Properties (6)</summary>
                        <div class="model assembly-model">
                           <div class="model-entry definition define-flag">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/task/associated-activities/activity-uuid" class="toc3 name">activity-uuid</h3>
                                 <p class="type"><a href="/reference/datatypes/#uuid">uuid</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/associated-activity/activity-uuid">Switch to XML</a></div>
                                 <p class="formal-name">Activity Universally Unique Identifier Reference</p>
                              </div>
                              <div class="body">
                                 <p class="description"><span class="usa-tag">description</span> A <a href="/concepts/identifier-use/#machine-oriented">machine-oriented</a> identifier reference to an activity defined in the list of activities.</p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/task/associated-activities/props" class="toc3 name">property</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/associated-activity/prop">Switch to XML</a></div>
                                 <p class="formal-name">Property</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">use name</span> <code class="name">prop</code></p>
                                 <p><span class="usa-tag">group as</span> <code class="name">props</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>Properties permit the deployment and management of arbitrary controlled values, within
                                             OSCAL objects. A property can be included for any purpose useful to an application
                                             or implementation. Typically, properties will be used to sort, filter, select, order,
                                             and arrange OSCAL content objects, to relate OSCAL objects to one another, or to associate
                                             an OSCAL object to class hierarchies, taxonomies, or external authorities. Thus, the
                                             lexical composition of properties may be constrained by external processes to ensure
                                             consistency.</p>
                                          <p>Property allows for associated remarks that describe why the specific property value
                                             was applied to the containing object, or the significance of the value in the context
                                             of the containing object.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/property">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/task/associated-activities/links" class="toc3 name">link</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/associated-activity/link">Switch to XML</a></div>
                                 <p class="formal-name">Link</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">group as</span> <code class="name">links</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>To provide a cryptographic hash for a remote target resource, a local reference to
                                             a back matter <code>resource</code> is needed. The resource allows one or more hash values to be provided using the <code>rlink/hash</code> object.</p>
                                          <p>The OSCAL <code>link</code> is a roughly based on the HTML <a href="https://www.w3.org/TR/html401/struct/links.html#edef-LINK">link element</a>. </p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/link">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/task/associated-activities/responsible-roles" class="toc3 name">responsible-role</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[0 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/associated-activity/responsible-role">Switch to XML</a></div>
                                 <p class="formal-name">Responsible Role</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">group as</span> <code class="name">responsible-roles</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>Identifies the person or organization responsible for performing a specific role defined
                                             by the activity.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-metadata/responsible-role">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition assembly">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/task/associated-activities/subjects" class="toc3 name">subject</h3>
                                 <p class="type">assembly<br class="br" /> </p>
                                 <p class="occurrence">[1 to ∞]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/associated-activity/subject">Switch to XML</a></div>
                                 <p class="formal-name">Subject of Assessment</p>
                              </div>
                              <div class="body">
                                 <p><span class="usa-tag">use name</span> <code class="name">subject</code></p>
                                 <p><span class="usa-tag">group as</span> <code class="name">subjects</code></p>
                                 <div class="remarks-group usa-prose">
                                    <details open="open">
                                       <summary class="subhead">Remarks</summary>
                                       <div class="remarks">
                                          <p>Processing of an include/exclude pair starts with processing the include, then removing
                                             matching entries in the exclude.</p>
                                       </div>
                                    </details>
                                 </div>
                                 <p class="definition-link"><a href="#/assembly/oscal-assessment-common/assessment-subject">See definition</a></p>
                              </div>
                           </div>
                           <div class="model-entry definition field">
                              <div class="instance-header">
                                 <h3 id="/assembly/oscal-assessment-common/task/associated-activities/remarks" class="toc3 name">remarks</h3>
                                 <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                                 <p class="occurrence">[0 or 1]</p>
                                 <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/associated-activity/remarks">Switch to XML</a></div>
                                 <p class="formal-name">Remarks</p>
                              </div>
                              <div class="body">
                                 <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                              </div>
                           </div>
                        </div>
                     </details>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/task/subjects" class="toc2 name">subject</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/subject">Switch to XML</a></div>
                     <p class="formal-name">Subject of Assessment</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">use name</span> <code class="name">subject</code></p>
                     <p><span class="usa-tag">group as</span> <code class="name">subjects</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Processing of an include/exclude pair starts with processing the include, then removing
                                 matching entries in the exclude.</p>
                           </div>
                           <div class="remarks">
                              <p>The assessment subjects that the activity was performed against.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-assessment-common/assessment-subject">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition assembly">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/task/responsible-roles" class="toc2 name">responsible-role</h2>
                     <p class="type">assembly<br class="br" /> </p>
                     <p class="occurrence">[0 to ∞]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/responsible-role">Switch to XML</a></div>
                     <p class="formal-name">Responsible Role</p>
                  </div>
                  <div class="body">
                     <p><span class="usa-tag">group as</span> <code class="name">responsible-roles</code></p>
                     <div class="remarks-group usa-prose">
                        <details open="open">
                           <summary class="subhead">Remarks</summary>
                           <div class="remarks">
                              <p>Identifies the person or organization responsible for performing a specific role related
                                 to the task.</p>
                           </div>
                        </details>
                     </div>
                     <p class="definition-link"><a href="#/assembly/oscal-metadata/responsible-role">See definition</a></p>
                  </div>
               </div>
               <div class="model-entry definition field">
                  <div class="instance-header">
                     <h2 id="/assembly/oscal-assessment-common/task/remarks" class="toc2 name">remarks</h2>
                     <p class="type"><a href="/reference/datatypes/#markup-multiline">markup-multiline</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/assembly/oscal-assessment-common/task/remarks">Switch to XML</a></div>
                     <p class="formal-name">Remarks</p>
                  </div>
                  <div class="body">
                     <p class="definition-link"><a href="#/field/oscal-metadata/remarks">See definition</a></p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-field">
      <div class="definition-header">
         <h1 id="/field/oscal-metadata/telephone-number" class="toc1 name">telephone-number</h1>
         <p class="type"><a href="/reference/datatypes/#string">string</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-metadata/telephone-number">Switch to XML</a></div>
         <p class="formal-name">Telephone Number</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> Contact number by telephone.</p>
         <p><span class="usa-tag">value key</span> <code class="name">number</code></p>
         <details open="open">
            <summary>Properties (2)</summary>
            <div class="model field-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/field/oscal-metadata/telephone-number/type" class="toc2 name">type</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-metadata/telephone-number/type">Switch to XML</a></div>
                     <p class="formal-name">type flag</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Indicates the type of phone number.</p>
                     <details>
                        <summary>Constraint (1)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed values</span></p>
                           <p>The value <b>may be locally defined</b>, or one of the following:</p>
                           <ul>
                              
                              <li><strong>home</strong>: A home phone number.</li>
                              
                              <li><strong>office</strong>: An office phone number.</li>
                              
                              <li><strong>mobile</strong>: A mobile phone number.</li>
                              </ul>
                        </div>
                        </details>
                  </div>
               </div>
               <div class="model-entry definition m:define-flag">
                  <div class="instance-header">
                     <h2 id="/field/oscal-metadata/telephone-number/number" class="toc2 name">number</h2>
                     <p class="type"><a href="/reference/datatypes/#string">string</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-metadata/telephone-number">Switch to XML</a></div>
                     <p class="formal-name">Telephone Number Value</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> This property provides the (nominal) value for this object as a whole.</p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-field">
      <div class="definition-header">
         <h1 id="/field/oscal-assessment-common/threat-id" class="toc1 name">threat-id</h1>
         <p class="type"><a href="/reference/datatypes/#uri">uri</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-assessment-common/threat-id">Switch to XML</a></div>
         <p class="formal-name">Threat ID</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A pointer, by ID, to an externally-defined threat.</p>
         <p><span class="usa-tag">value key</span> <code class="name">id</code></p>
         <details open="open">
            <summary>Properties (3)</summary>
            <div class="model field-model">
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/field/oscal-assessment-common/threat-id/system" class="toc2 name">system</h2>
                     <p class="type"><a href="/reference/datatypes/#uri">uri</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-assessment-common/threat-id/system">Switch to XML</a></div>
                     <p class="formal-name">Threat Type Identification System</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> Specifies the source of the threat information.</p>
                     <details>
                        <summary>Constraint (1)</summary>
                        
                        <div class="constraint">
                           <p><span class="usa-tag">allowed value</span></p>
                           <p>The value <b>may be locally defined</b>, or the following:</p>
                           <ul>
                              
                              <li><strong>https://fedramp.gov</strong>: The value conforms to FedRAMP definitions.</li>
                              </ul>
                        </div>
                        </details>
                  </div>
               </div>
               <div class="model-entry definition define-flag">
                  <div class="instance-header">
                     <h2 id="/field/oscal-assessment-common/threat-id/href" class="toc2 name">href</h2>
                     <p class="type"><a href="/reference/datatypes/#uri-reference">uri-reference</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-assessment-common/threat-id/href">Switch to XML</a></div>
                     <p class="formal-name">Threat Information Resource Reference</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> An optional location for the threat data, from which this ID originates.</p>
                  </div>
               </div>
               <div class="model-entry definition m:define-flag">
                  <div class="instance-header">
                     <h2 id="/field/oscal-assessment-common/threat-id/id" class="toc2 name">id</h2>
                     <p class="type"><a href="/reference/datatypes/#uri">uri</a></p>
                     <p class="occurrence">[0 or 1]</p>
                     <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-assessment-common/threat-id">Switch to XML</a></div>
                     <p class="formal-name">Threat ID Value</p>
                  </div>
                  <div class="body">
                     <p class="description"><span class="usa-tag">description</span> This property provides the (nominal) value for this object as a whole.</p>
                  </div>
               </div>
            </div>
         </details>
      </div>
   </div>
   <div class="model-entry definition define-field">
      <div class="definition-header">
         <h1 id="/field/oscal-metadata/version" class="toc1 name">version</h1>
         <p class="type"><a href="/reference/datatypes/#string">string</a></p>
         <div class="crosslink"><a class="usa-button" href="../xml-definitions/#/field/oscal-metadata/version">Switch to XML</a></div>
         <p class="formal-name">Document Version</p>
      </div>
      <div class="body">
         <p class="description"><span class="usa-tag">description</span> A string used to distinguish the current version of the document from other previous
            (and future) versions.</p>
         <div class="remarks-group usa-prose">
            <details open="open">
               <summary class="subhead">Remarks</summary>
               <div class="remarks">
                  <p>A version string may be a release number, sequence number, date, or other identifier
                     suffcient to distinguish between different document versions. This version is typically
                     set by the document owner or by the tool used to maintain the content.</p>
                  <p>While not required, it is recommended that OSCAL content authors use <a href="https://semver.org/spec/v2.0.0.html">Semantic Versioning</a> as a format for version strings. This allows for the easy identification of a version
                     tree consisting of major, minor, and patch numbers.</p>
                  <p>A publisher of OSCAL content can use this data point along with its siblings <code>published</code> and <code>last-modified</code> to establish a sequence of successive revisions of a given OSCAL-based publication.
                     The metadata for previous revisions can be represented as a <code>revision</code> in this object.</p>
               </div>
            </details>
         </div>
      </div>
   </div>
</div>{{< /rawhtml >}}
