---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: a18222c40dc5c56bd2d67afb8d0df35b7aedc532
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942740"
---
# <span data-ttu-id="6f804-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="6f804-101">Get-AzAttestation</span></span>

## <span data-ttu-id="6f804-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6f804-102">SYNOPSIS</span></span>
<span data-ttu-id="6f804-103">Recebe um atestado.</span><span class="sxs-lookup"><span data-stu-id="6f804-103">Gets an attestation.</span></span>

## <span data-ttu-id="6f804-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f804-104">SYNTAX</span></span>

### <span data-ttu-id="6f804-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6f804-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6f804-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f804-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f804-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6f804-107">DESCRIPTION</span></span>
<span data-ttu-id="6f804-108">O cmdlet Get-AzAttestation Obtém informações sobre o atestado em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="6f804-108">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="6f804-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6f804-109">EXAMPLES</span></span>

### <span data-ttu-id="6f804-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6f804-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestation -Name pshtest -ResourceGroupName psh-test-rg                                                                                                                                                                                                                                                       
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest
Status            : Ready
TrustModel        : AAD
AttestUri         : https://pshtest.us.attest.azure.net
Tags              : {Production, Example}
TagsTable         :
                    Name        Value
                    ==========  =====
                    Production  False
                    Example     True
```

<span data-ttu-id="6f804-111">Obter provedor de atestado *pshtest* no grupo de recursos *PSH-Test-RG*.</span><span class="sxs-lookup"><span data-stu-id="6f804-111">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

## <span data-ttu-id="6f804-112">OS</span><span class="sxs-lookup"><span data-stu-id="6f804-112">PARAMETERS</span></span>

### <span data-ttu-id="6f804-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f804-113">-DefaultProfile</span></span>
<span data-ttu-id="6f804-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6f804-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f804-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6f804-115">-Name</span></span>
<span data-ttu-id="6f804-116">Nome do atestado.</span><span class="sxs-lookup"><span data-stu-id="6f804-116">Attestation Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f804-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f804-117">-ResourceGroupName</span></span>
<span data-ttu-id="6f804-118">Especifica o nome do grupo de recursos associado ao atestado que está sendo consultado.</span><span class="sxs-lookup"><span data-stu-id="6f804-118">Specifies the name of the resource group associated with the attestation being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f804-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f804-119">-ResourceId</span></span>
<span data-ttu-id="6f804-120">Especifica o nome da ResourceId associada ao atestado que está sendo consultado</span><span class="sxs-lookup"><span data-stu-id="6f804-120">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

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

### <span data-ttu-id="6f804-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f804-121">CommonParameters</span></span>
<span data-ttu-id="6f804-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f804-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f804-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f804-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f804-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6f804-124">INPUTS</span></span>

### <span data-ttu-id="6f804-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6f804-125">System.String</span></span>

## <span data-ttu-id="6f804-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6f804-126">OUTPUTS</span></span>

### <span data-ttu-id="6f804-127">Microsoft. Azure. Commands.. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="6f804-127">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="6f804-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6f804-128">NOTES</span></span>

## <span data-ttu-id="6f804-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f804-129">RELATED LINKS</span></span>
