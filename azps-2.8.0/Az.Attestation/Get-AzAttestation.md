---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: cd6181ffb2bba8d71d8a0bf7cbe96d2f8038efc5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597884"
---
# <span data-ttu-id="02d5d-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="02d5d-101">Get-AzAttestation</span></span>

## <span data-ttu-id="02d5d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02d5d-102">SYNOPSIS</span></span>
<span data-ttu-id="02d5d-103">Recebe um atestado.</span><span class="sxs-lookup"><span data-stu-id="02d5d-103">Gets an attestation.</span></span>

## <span data-ttu-id="02d5d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02d5d-104">SYNTAX</span></span>

### <span data-ttu-id="02d5d-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="02d5d-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="02d5d-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="02d5d-106">ResourceGroupParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02d5d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02d5d-107">DESCRIPTION</span></span>
<span data-ttu-id="02d5d-108">O cmdlet Get-AzAttestation Obtém informações sobre o atestado em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="02d5d-108">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="02d5d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02d5d-109">EXAMPLES</span></span>

### <span data-ttu-id="02d5d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="02d5d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestation -Name example -ResourceGroupName rg1 
Id                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/rg1/providers/Microsoft.Attestation/attestationProviders/example
Name                : example
Type                : Microsoft.Attestation/attestationProviders
Status              : Ready
AttesUri            : https://example.us.attest.azure.net
ResoureGroupName    : rg1 
SubscriptionId      : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
```
<span data-ttu-id="02d5d-111">Obter o atestado "exemplo" no grupo de recursos "Rg1".</span><span class="sxs-lookup"><span data-stu-id="02d5d-111">Get Attestation "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="02d5d-112">OS</span><span class="sxs-lookup"><span data-stu-id="02d5d-112">PARAMETERS</span></span>

### <span data-ttu-id="02d5d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02d5d-113">-DefaultProfile</span></span>
<span data-ttu-id="02d5d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02d5d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02d5d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="02d5d-115">-Name</span></span>
<span data-ttu-id="02d5d-116">Nome do atestado.</span><span class="sxs-lookup"><span data-stu-id="02d5d-116">Attestation Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02d5d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02d5d-117">-ResourceGroupName</span></span>
<span data-ttu-id="02d5d-118">Especifica o nome do grupo de recursos associado ao atestado que está sendo consultado.</span><span class="sxs-lookup"><span data-stu-id="02d5d-118">Specifies the name of the resource group associated with the attestation being queried.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02d5d-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02d5d-119">-ResourceId</span></span>
<span data-ttu-id="02d5d-120">Especifica o nome da ResourceId associada ao atestado que está sendo consultado</span><span class="sxs-lookup"><span data-stu-id="02d5d-120">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02d5d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02d5d-121">CommonParameters</span></span>
<span data-ttu-id="02d5d-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02d5d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02d5d-123">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02d5d-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02d5d-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02d5d-124">INPUTS</span></span>

### <span data-ttu-id="02d5d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="02d5d-125">System.String</span></span>

## <span data-ttu-id="02d5d-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02d5d-126">OUTPUTS</span></span>

### <span data-ttu-id="02d5d-127">Microsoft. Azure. Commands.. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="02d5d-127">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="02d5d-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02d5d-128">NOTES</span></span>

## <span data-ttu-id="02d5d-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02d5d-129">RELATED LINKS</span></span>
