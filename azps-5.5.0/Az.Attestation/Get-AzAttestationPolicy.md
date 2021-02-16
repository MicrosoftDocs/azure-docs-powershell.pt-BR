---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
ms.openlocfilehash: 64a74902d1a5b10ed36c635b58910246634e68b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127138"
---
# <span data-ttu-id="b825f-101">Get-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="b825f-101">Get-AzAttestationPolicy</span></span>

## <span data-ttu-id="b825f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b825f-102">SYNOPSIS</span></span>
<span data-ttu-id="b825f-103">Obtém a política de um locatário no Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="b825f-103">Gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="b825f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b825f-104">SYNTAX</span></span>

### <span data-ttu-id="b825f-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b825f-105">NameParameterSet</span></span>
```
Get-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b825f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b825f-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b825f-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="b825f-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestationPolicy [-Location] <String> [-DefaultProvider] -Tee <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b825f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b825f-108">DESCRIPTION</span></span>
<span data-ttu-id="b825f-109">O Get-AzAttestationPolicy cmdlet obtém a política de um locatário no Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="b825f-109">The Get-AzAttestationPolicy cmdlet gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="b825f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b825f-110">EXAMPLES</span></span>

### <span data-ttu-id="b825f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b825f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave                                                                                                                                                                                                                    
Text       : version= 1.0;
             authorizationrules{
                 c:[type=="$is-debuggable"] => permit();
             };
             issuancerules{
                 c:[type=="$is-debuggable"] => issue(type="is-debuggable", value=c.value);
                 c:[type=="$sgx-mrsigner"] => issue(type="sgx-mrsigner", value=c.value);
                 c:[type=="$sgx-mrenclave"] => issue(type="sgx-mrenclave", value=c.value);
                 c:[type=="$product-id"] => issue(type="product-id", value=c.value);
                 c:[type=="$svn"] => issue(type="svn", value=c.value);
                 c:[type=="$tee"] => issue(type="tee", value=c.value);
                 c:[type=="$tee-future"] => issue(type="tee-future", value=c.value);
             };

TextLength : 604
Jwt        : eyJhbGciOiJub25lIn0.eyJBdHRlc3RhdGlvblBvbGljeSI6ICJkbVZ5YzJsdmJqMGdNUzR3T3cwS1lYVjBhRzl5YVhwaGRHbHZibkoxYkdWemV3MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2FYTXRaR1ZpZFdkbllXSnNaU0pkSUQwLUlIQmxjbTFwZENncE93MEtmVHNOQ21semMzVmhibU5sY25Wc1pYTjdEUW9nSUNBZ1l6cGJkSGx3WlQwOUlpUnBjeTFrWldKMVoyZGhZbXhsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYVhNdFpHVmlkV2RuWVdKc1pTSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE93MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2MyZDRMVzF5YzJsbmJtVnlJbDBnUFQ0Z2FYTnpkV1VvZEhsd1pUMGljMmQ0TFcxeWMybG5ibVZ5SWl3Z2RtRnNkV1U5WXk1MllXeDFaU2s3RFFvZ0lDQWdZenBiZEhsd1pUMDlJaVJ6WjNndGJYSmxibU5zWVhabElsMGdQVDRnYVhOemRXVW9kSGx3WlQwaWMyZDRMVzF5Wlc1amJHRjJaU0lzSUhaaGJIVmxQV011ZG1Gc2RXVXBPdzBLSUNBZ0lHTTZXM1I1Y0dVOVBTSWtjSEp2WkhWamRDMXBaQ0pkSUQwLUlHbHpjM1ZsS0hSNWNHVTlJbkJ5YjJSMVkzUXRhV1FpTENCMllXeDFaVDFqTG5aaGJIVmxLVHNOQ2lBZ0lDQmpPbHQwZVhCbFBUMGlKSE4yYmlKZElEMC1JR2x6YzNWbEtIUjVjR1U5SW5OMmJpSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE93MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2RHVmxJbDBnUFQ0Z2FYTnpkV1VvZEhsd1pUMGlkR1ZsSWl3Z2RtRnNkV1U5WXk1MllXeDFaU2s3RFFvZ0lDQWdZenBiZEhsd1pUMDlJaVIwWldVdFpuVjBkWEpsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpZEdWbExXWjFkSFZ5WlNJc0lIWmhiSFZsUFdNdWRtRnNkV1VwT3cwS2ZUc05DZyJ9.
JwtLength  : 1129
Algorithm  : none
```

<span data-ttu-id="b825f-112">Obtém a política de teste *pshtest* do Provedor de Teste para Tipo de Tee *SgxEn ltda.*</span><span class="sxs-lookup"><span data-stu-id="b825f-112">Gets the policy for Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="b825f-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b825f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAttestationPolicy -DefaultProvider -Location "UK South" -Tee SgxEnclave
Text       : version= 1.0;authorizationrules{c:[type=="$is-debuggable"] => permit();};issuancerules{c:[type=="$is-debuggable"] => issue(type="is-debuggable",
             value=c.value);c:[type=="$sgx-mrsigner"] => issue(type="sgx-mrsigner", value=c.value);c:[type=="$sgx-mrenclave"] => issue(type="sgx-mrenclave",
             value=c.value);c:[type=="$product-id"] => issue(type="product-id", value=c.value);c:[type=="$svn"] => issue(type="svn", value=c.value);c:[type=="$tee"]
             => issue(type="tee", value=c.value);};
TextLength : 479
Jwt        : eyJhbGciOiJub25lIn0.eyJBdHRlc3RhdGlvblBvbGljeSI6ICJkbVZ5YzJsdmJqMGdNUzR3TzJGMWRHaHZjbWw2WVhScGIyNXlkV3hsYzN0ak9sdDBlWEJsUFQwaUpHbHpMV1JsWW5WbloyRmliR1Vp
             WFNBOVBpQndaWEp0YVhRb0tUdDlPMmx6YzNWaGJtTmxjblZzWlhON1l6cGJkSGx3WlQwOUlpUnBjeTFrWldKMVoyZGhZbXhsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYVhNdFpHVmlkV2RuWVdKc1pT
             SXNJSFpoYkhWbFBXTXVkbUZzZFdVcE8yTTZXM1I1Y0dVOVBTSWtjMmQ0TFcxeWMybG5ibVZ5SWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYzJkNExXMXljMmxuYm1WeUlpd2dkbUZzZFdVOVl5NTJZV3gx
             WlNrN1l6cGJkSGx3WlQwOUlpUnpaM2d0YlhKbGJtTnNZWFpsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYzJkNExXMXlaVzVqYkdGMlpTSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE8yTTZXM1I1Y0dVOVBT
             SWtjSEp2WkhWamRDMXBaQ0pkSUQwLUlHbHpjM1ZsS0hSNWNHVTlJbkJ5YjJSMVkzUXRhV1FpTENCMllXeDFaVDFqTG5aaGJIVmxLVHRqT2x0MGVYQmxQVDBpSkhOMmJpSmRJRDAtSUdsemMzVmxLSFI1
             Y0dVOUluTjJiaUlzSUhaaGJIVmxQV011ZG1Gc2RXVXBPMk02VzNSNWNHVTlQU0lrZEdWbElsMGdQVDRnYVhOemRXVW9kSGx3WlQwaWRHVmxJaXdnZG1Gc2RXVTlZeTUyWVd4MVpTazdmVHMifQ.
JwtLength  : 907
Algorithm  : none
```

<span data-ttu-id="b825f-114">Obtém a política para o Provedor Padrão de Teste da Location *UK South* para o tipo *de tee SgxEnmaxe.*</span><span class="sxs-lookup"><span data-stu-id="b825f-114">Gets the policy for Attestation Default Provider from Location *UK South* for Tee type *SgxEnclave*.</span></span>

## <span data-ttu-id="b825f-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b825f-115">PARAMETERS</span></span>

### <span data-ttu-id="b825f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b825f-116">-DefaultProfile</span></span>
<span data-ttu-id="b825f-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b825f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b825f-118">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="b825f-118">-DefaultProvider</span></span>
<span data-ttu-id="b825f-119">Especifica que essa é a solicitação para um provedor de teste padrão.</span><span class="sxs-lookup"><span data-stu-id="b825f-119">Specifies this is the request to a default attestation provider.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b825f-120">-Local</span><span class="sxs-lookup"><span data-stu-id="b825f-120">-Location</span></span>
<span data-ttu-id="b825f-121">Especifica a Localização do provedor de teste padrão.</span><span class="sxs-lookup"><span data-stu-id="b825f-121">Specifies the Location of the default attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b825f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b825f-122">-Name</span></span>
<span data-ttu-id="b825f-123">Especifica um nome do locatário.</span><span class="sxs-lookup"><span data-stu-id="b825f-123">Specifies a name of the tenant.</span></span>
<span data-ttu-id="b825f-124">Este cmdlet obtém a política de teste para o locatário especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b825f-124">This cmdlet gets the attestation policy for the tenant that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b825f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b825f-125">-ResourceGroupName</span></span>
<span data-ttu-id="b825f-126">Especifica o nome do grupo de recursos de um provedor de teste.</span><span class="sxs-lookup"><span data-stu-id="b825f-126">Specifies the resource group name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b825f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b825f-127">-ResourceId</span></span>
<span data-ttu-id="b825f-128">Especifica a ResourceID de um provedor de teste.</span><span class="sxs-lookup"><span data-stu-id="b825f-128">Specifies the ResourceID of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b825f-129">-Tee</span><span class="sxs-lookup"><span data-stu-id="b825f-129">-Tee</span></span>
<span data-ttu-id="b825f-130">Especifica um tipo de Ambiente de Execução Confiável.</span><span class="sxs-lookup"><span data-stu-id="b825f-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="b825f-131">Há suporte para quatro tipos de ambiente: SgxEntronice, OpenEn ltda, CyResComponent e VBSEn ltda.</span><span class="sxs-lookup"><span data-stu-id="b825f-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b825f-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b825f-132">-Confirm</span></span>
<span data-ttu-id="b825f-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b825f-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b825f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b825f-134">-WhatIf</span></span>
<span data-ttu-id="b825f-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b825f-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b825f-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b825f-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b825f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b825f-137">CommonParameters</span></span>
<span data-ttu-id="b825f-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b825f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b825f-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b825f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b825f-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="b825f-140">INPUTS</span></span>

### <span data-ttu-id="b825f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b825f-141">System.String</span></span>

## <span data-ttu-id="b825f-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="b825f-142">OUTPUTS</span></span>

### <span data-ttu-id="b825f-143">Microsoft.Azure.Commands.Attestation.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="b825f-143">Microsoft.Azure.Commands.Attestation.Models.PSPolicy</span></span>

## <span data-ttu-id="b825f-144">Notas</span><span class="sxs-lookup"><span data-stu-id="b825f-144">NOTES</span></span>

## <span data-ttu-id="b825f-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b825f-145">RELATED LINKS</span></span>
