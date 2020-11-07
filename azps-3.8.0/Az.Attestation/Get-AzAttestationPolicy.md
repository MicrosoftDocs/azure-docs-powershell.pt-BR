---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
ms.openlocfilehash: 0c36f5fb87e3d247a48031bdc735c077a577ac27
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942735"
---
# <span data-ttu-id="b1a65-101">Get-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="b1a65-101">Get-AzAttestationPolicy</span></span>

## <span data-ttu-id="b1a65-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b1a65-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a65-103">Obtém a política de um locatário no Azure atestado.</span><span class="sxs-lookup"><span data-stu-id="b1a65-103">Gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="b1a65-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1a65-104">SYNTAX</span></span>

### <span data-ttu-id="b1a65-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1a65-105">NameParameterSet</span></span>
```
Get-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1a65-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1a65-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1a65-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b1a65-107">DESCRIPTION</span></span>
<span data-ttu-id="b1a65-108">O cmdlet Get-AzAttestationPolicy Obtém a política de um locatário no Azure atestado.</span><span class="sxs-lookup"><span data-stu-id="b1a65-108">The Get-AzAttestationPolicy cmdlet gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="b1a65-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b1a65-109">EXAMPLES</span></span>

### <span data-ttu-id="b1a65-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b1a65-110">Example 1</span></span>
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

<span data-ttu-id="b1a65-111">Obtém a política para o provedor de atestado *pshtest* para o tipo de *SgxEnclave*.</span><span class="sxs-lookup"><span data-stu-id="b1a65-111">Gets the policy for Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

## <span data-ttu-id="b1a65-112">OS</span><span class="sxs-lookup"><span data-stu-id="b1a65-112">PARAMETERS</span></span>

### <span data-ttu-id="b1a65-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1a65-113">-DefaultProfile</span></span>
<span data-ttu-id="b1a65-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b1a65-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1a65-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1a65-115">-Name</span></span>
<span data-ttu-id="b1a65-116">Especifica um nome do locatário.</span><span class="sxs-lookup"><span data-stu-id="b1a65-116">Specifies a name of the tenant.</span></span>
<span data-ttu-id="b1a65-117">Esse cmdlet obtém a política de atestado para o locatário que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b1a65-117">This cmdlet gets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="b1a65-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1a65-118">-ResourceGroupName</span></span>
<span data-ttu-id="b1a65-119">Especifica o nome do grupo de recursos de um provedor de atestado.</span><span class="sxs-lookup"><span data-stu-id="b1a65-119">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="b1a65-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1a65-120">-ResourceId</span></span>
<span data-ttu-id="b1a65-121">Especifica o ResourceId de um provedor de atestado.</span><span class="sxs-lookup"><span data-stu-id="b1a65-121">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="b1a65-122">-T</span><span class="sxs-lookup"><span data-stu-id="b1a65-122">-Tee</span></span>
<span data-ttu-id="b1a65-123">Especifica um tipo de ambiente de execução confiável.</span><span class="sxs-lookup"><span data-stu-id="b1a65-123">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="b1a65-124">Oferecemos suporte a quatro tipos de ambiente: SgxEnclave, OpenEnclave, CyResComponent e VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="b1a65-124">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="b1a65-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b1a65-125">-Confirm</span></span>
<span data-ttu-id="b1a65-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1a65-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1a65-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1a65-127">-WhatIf</span></span>
<span data-ttu-id="b1a65-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b1a65-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1a65-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b1a65-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1a65-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a65-130">CommonParameters</span></span>
<span data-ttu-id="b1a65-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1a65-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a65-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1a65-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a65-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b1a65-133">INPUTS</span></span>

### <span data-ttu-id="b1a65-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b1a65-134">System.String</span></span>

## <span data-ttu-id="b1a65-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b1a65-135">OUTPUTS</span></span>

### <span data-ttu-id="b1a65-136">Microsoft. Azure. Commands.. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="b1a65-136">Microsoft.Azure.Commands.Attestation.Models.PSPolicy</span></span>

## <span data-ttu-id="b1a65-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b1a65-137">NOTES</span></span>

## <span data-ttu-id="b1a65-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1a65-138">RELATED LINKS</span></span>
