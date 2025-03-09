# Facebook Ad Tracking Considerations

## Current Tracking Issue

### Observed Discrepancy
- **Facebook Reports**: 13 link clicks across campaigns
- **Website Analytics**: No tracked views on landing page
- **Conversion Data**: No survey completions

This tracking gap needs to be addressed to properly evaluate campaign performance and optimize for the right metrics.

## Common Causes of Tracking Discrepancies

### Technical Implementation Issues
1. **Facebook Pixel Integration**:
   - Pixel may not be properly installed on landing page
   - Pixel may be blocked by ad blockers or browser privacy features
   - Pixel event codes may not be firing correctly

2. **URL Parameters**:
   - Missing or improper UTM parameters in ad URLs
   - Broken redirect chains losing parameter data

3. **User Experience Issues**:
   - Page load speed issues causing abandonments before tracking fires
   - Mobile compatibility problems
   - Browser compatibility issues

4. **Third-Party Interference**:
   - Ad blockers preventing tracking scripts from loading
   - Privacy browsers blocking tracking cookies
   - VPN or proxy services affecting attribution

## Recommended Tracking Solutions

### Immediate Technical Fixes
1. **Verify Facebook Pixel Implementation**:
   - Use Facebook Pixel Helper browser extension to check for proper firing
   - Review browser console for JavaScript errors
   - Ensure pixel base code is in the `<head>` section of all pages

2. **Implement Robust UTM Parameters**:
   ```
   ?utm_source=facebook&utm_medium=cpc&utm_campaign=it_consultants&utm_content=math_wall&utm_term=apply_now
   ```

3. **Test Landing Page Technical Performance**:
   - Run page speed tests (aim for < 3 second load time)
   - Test on multiple devices and browsers
   - Check mobile responsiveness

### Comprehensive Tracking Implementation

1. **"Sandwich" Tracking Approach**:
   - Implement multiple tracking methods to compare data
   - Primary: Facebook Pixel
   - Secondary: Google Analytics
   - Tertiary: Direct conversion tracking on form submission

2. **Server-Side Tracking**:
   - Implement Facebook Conversion API (less susceptible to browser limitations)
   - Server-side Google Analytics
   - First-party cookie implementation

3. **User-Reported Attribution**:
   - Add "How did you hear about us?" field to forms
   - Include Facebook Ads as an option
   - Use this as backup verification for other tracking methods

## Performance Measurement Strategy

### Metrics Reliability Hierarchy
When evaluating performance with imperfect tracking:

1. **Most Reliable**: Actual leads/conversions (verify source manually)
2. **Moderately Reliable**: Landing page engagement metrics (time on page, scroll depth)
3. **Less Reliable**: Facebook-reported clicks (directional but not absolute)
4. **Least Reliable**: Facebook-reported impressions (awareness only)

### Campaign Optimization Approach

While addressing tracking issues:
1. Focus optimization on Facebook-reported metrics (CTR, CPC)
2. Conduct manual verification of lead quality
3. Implement progressive tracking improvements
4. Gradually shift to conversion-based optimization once tracking is reliable

## Implementation Timeline

### Short-Term (1-3 Days)
- Verify Facebook pixel implementation
- Add UTM parameters to all ad URLs
- Test landing page on multiple devices

### Medium-Term (1-2 Weeks)
- Implement Google Analytics tracking
- Add user-reported attribution field to forms
- Document Facebook-to-website analytics differences

### Long-Term (2-4 Weeks)
- Implement server-side tracking
- Develop comprehensive attribution model
- Create automated reporting that reconciles data sources

## Conclusion

Addressing tracking discrepancies is critical for campaign optimization. While technical solutions are implemented, campaign decisions should be based on the most reliable available data, with the understanding that perfect attribution may not be immediately achievable.

*Last updated: March 8, 2025*