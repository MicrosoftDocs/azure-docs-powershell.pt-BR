---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: 650ac7c478f1c27ca3ba925c4d767f02c79fa781
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116639"
---
# <span data-ttu-id="0891a-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="0891a-101">Get-AzAttestation</span></span>

## <span data-ttu-id="0891a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0891a-102">SYNOPSIS</span></span>
<span data-ttu-id="0891a-103">Obtém um teste.</span><span class="sxs-lookup"><span data-stu-id="0891a-103">Gets an attestation.</span></span>

## <span data-ttu-id="0891a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0891a-104">SYNTAX</span></span>

### <span data-ttu-id="0891a-105">NameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0891a-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0891a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0891a-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0891a-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="0891a-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestation [[-Location] <String>] [-DefaultProvider] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0891a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0891a-108">DESCRIPTION</span></span>
<span data-ttu-id="0891a-109">O Get-AzAttestation cmdlet obtém informações sobre o teste em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="0891a-109">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="0891a-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0891a-110">EXAMPLES</span></span>

### <span data-ttu-id="0891a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0891a-111">Example 1</span></span>
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

<span data-ttu-id="0891a-112">Obter teste *pshtest* do Provedor de Teste de Recurso no Resource Group *psh-test-rg.*</span><span class="sxs-lookup"><span data-stu-id="0891a-112">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

### <span data-ttu-id="0891a-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0891a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAttestation -DefaultProvider
Id                : /providers/Microsoft.Attestation/attestationProviders/sharedeus2
Location          : East US 2
ResourceGroupName :
Name              : sharedeus2
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedeus2.eus2.attest.azure.net
Tags              :
TagsTable         :

Id                : /providers/Microsoft.Attestation/attestationProviders/sharedcus
Location          : Central US
ResourceGroupName :
Name              : sharedcus
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedcus.cus.attest.azure.net
Tags              :
TagsTable         :

Id                : /providers/Microsoft.Attestation/attestationProviders/shareduks
Location          : UK South
ResourceGroupName :
Name              : shareduks
Status            : Ready
TrustModel        : AAD
AttestUri         : https://shareduks.uks.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="0891a-114">Obter todos os Provedores Padrão de Teste disponíveis</span><span class="sxs-lookup"><span data-stu-id="0891a-114">Get all available Attestation Default Providers</span></span>

### <span data-ttu-id="0891a-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0891a-115">Example 3</span></span>
```powershell
PS C:\> Get-AzAttestation -DefaultProvider -Location "East US 2"
Id                : /providers/Microsoft.Attestation/attestationProviders/sharedeus2
Location          : East US 2
ResourceGroupName :
Name              : sharedeus2
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedeus2.eus2.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="0891a-116">Obter Provedor Padrão de Teste da Localização *leste dos EUA 2*</span><span class="sxs-lookup"><span data-stu-id="0891a-116">Get Attestation Default Provider from Location *East US 2*</span></span>

## <span data-ttu-id="0891a-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0891a-117">PARAMETERS</span></span>

### <span data-ttu-id="0891a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0891a-118">-DefaultProfile</span></span>
<span data-ttu-id="0891a-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0891a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0891a-120">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="0891a-120">-DefaultProvider</span></span>
<span data-ttu-id="0891a-121">Especifica que essa é a solicitação para um provedor de teste padrão.</span><span class="sxs-lookup"><span data-stu-id="0891a-121">Specifies this is the request to a default attestation provider.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0891a-122">-Local</span><span class="sxs-lookup"><span data-stu-id="0891a-122">-Location</span></span>
<span data-ttu-id="0891a-123">Especifica a Localização do provedor de teste padrão.</span><span class="sxs-lookup"><span data-stu-id="0891a-123">Specifies the Location of the default attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0891a-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="0891a-124">-Name</span></span>
<span data-ttu-id="0891a-125">Nome de teste.</span><span class="sxs-lookup"><span data-stu-id="0891a-125">Attestation Name.</span></span>

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

### <span data-ttu-id="0891a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0891a-126">-ResourceGroupName</span></span>
<span data-ttu-id="0891a-127">Especifica o nome do grupo de recursos associado ao teste que está sendo consultado.</span><span class="sxs-lookup"><span data-stu-id="0891a-127">Specifies the name of the resource group associated with the attestation being queried.</span></span>

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

### <span data-ttu-id="0891a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0891a-128">-ResourceId</span></span>
<span data-ttu-id="0891a-129">Especifica o nome da IDdo Recurso associada ao teste que está sendo consultado</span><span class="sxs-lookup"><span data-stu-id="0891a-129">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

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

### <span data-ttu-id="0891a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0891a-130">CommonParameters</span></span>
<span data-ttu-id="0891a-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0891a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0891a-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0891a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0891a-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="0891a-133">INPUTS</span></span>

### <span data-ttu-id="0891a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="0891a-134">System.String</span></span>

## <span data-ttu-id="0891a-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="0891a-135">OUTPUTS</span></span>

### <span data-ttu-id="0891a-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="0891a-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="0891a-137">Notas</span><span class="sxs-lookup"><span data-stu-id="0891a-137">NOTES</span></span>

## <span data-ttu-id="0891a-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0891a-138">RELATED LINKS</span></span>
