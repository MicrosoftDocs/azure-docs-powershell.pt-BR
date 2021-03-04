---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/powershell/module/az.maps/get-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
ms.openlocfilehash: bce5110a4aa03686b8ae38ee03ea853bc6c89949
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890836"
---
# <span data-ttu-id="a15ad-101">Get-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="a15ad-101">Get-AzMapsAccountKey</span></span>

## <span data-ttu-id="a15ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a15ad-102">SYNOPSIS</span></span>
<span data-ttu-id="a15ad-103">Obtém as chaves da API de uma conta.</span><span class="sxs-lookup"><span data-stu-id="a15ad-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="a15ad-104">Essas chaves são o mecanismo de autenticação usado em chamadas subsequentes para mapas do Azure.</span><span class="sxs-lookup"><span data-stu-id="a15ad-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

## <span data-ttu-id="a15ad-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a15ad-105">SYNTAX</span></span>

### <span data-ttu-id="a15ad-106">NameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a15ad-106">NameParameterSet (Default)</span></span>
```
Get-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a15ad-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a15ad-107">InputObjectParameterSet</span></span>
```
Get-AzMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a15ad-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a15ad-108">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a15ad-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a15ad-109">DESCRIPTION</span></span>
<span data-ttu-id="a15ad-110">O Get-AzMapsAccountKey cmdlet obtém as chaves da API de uma conta provisionada do Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="a15ad-110">The Get-AzMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="a15ad-111">Uma conta do Azure Maps tem duas chaves de API: Primária e Secundária.</span><span class="sxs-lookup"><span data-stu-id="a15ad-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="a15ad-112">As teclas habilitam a interação com o ponto de extremidade da conta do Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="a15ad-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="a15ad-113">Use New-AzMapsAccountKey (New-AzMapsAccountKey.md)para regenerar uma chave.</span><span class="sxs-lookup"><span data-stu-id="a15ad-113">Use New-AzMapsAccountKey (New-AzMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="a15ad-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a15ad-114">EXAMPLES</span></span>

### <span data-ttu-id="a15ad-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a15ad-115">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="a15ad-116">Retorna as chaves da conta chamada MyAccount no grupo de recursos MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a15ad-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="a15ad-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a15ad-117">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="a15ad-118">Retorna as chaves da Conta de Mapas do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="a15ad-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="a15ad-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a15ad-119">PARAMETERS</span></span>

### <span data-ttu-id="a15ad-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a15ad-120">-DefaultProfile</span></span>
<span data-ttu-id="a15ad-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a15ad-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a15ad-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a15ad-122">-InputObject</span></span>
<span data-ttu-id="a15ad-123">Mapas Conta canalização de Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="a15ad-123">Maps Account piped from Get-AzMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a15ad-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a15ad-124">-Name</span></span>
<span data-ttu-id="a15ad-125">Mapeia o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="a15ad-125">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a15ad-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a15ad-126">-ResourceGroupName</span></span>
<span data-ttu-id="a15ad-127">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="a15ad-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="a15ad-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a15ad-128">-ResourceId</span></span>
<span data-ttu-id="a15ad-129">Mapeia ResourceId da conta.</span><span class="sxs-lookup"><span data-stu-id="a15ad-129">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="a15ad-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a15ad-130">CommonParameters</span></span>
<span data-ttu-id="a15ad-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a15ad-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a15ad-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a15ad-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a15ad-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a15ad-133">INPUTS</span></span>

### <span data-ttu-id="a15ad-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a15ad-134">System.String</span></span>

### <span data-ttu-id="a15ad-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="a15ad-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="a15ad-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a15ad-136">OUTPUTS</span></span>

### <span data-ttu-id="a15ad-137">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a15ad-137">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="a15ad-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="a15ad-138">NOTES</span></span>

## <span data-ttu-id="a15ad-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a15ad-139">RELATED LINKS</span></span>
