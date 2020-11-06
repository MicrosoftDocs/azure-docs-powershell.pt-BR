---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/get-azurermmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccountKey.md
ms.openlocfilehash: 1afe0f8f93bd00a384e1bb741ed8ea54e1ae66d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430878"
---
# <span data-ttu-id="c380f-101">Get-AzureRmMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="c380f-101">Get-AzureRmMapsAccountKey</span></span>

## <span data-ttu-id="c380f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c380f-102">SYNOPSIS</span></span>
<span data-ttu-id="c380f-103">Obtém as chaves de API para uma conta.</span><span class="sxs-lookup"><span data-stu-id="c380f-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="c380f-104">Essas chaves são o mecanismo de autenticação usado em chamadas subsequentes para mapas do Azure.</span><span class="sxs-lookup"><span data-stu-id="c380f-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c380f-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c380f-105">SYNTAX</span></span>

### <span data-ttu-id="c380f-106">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c380f-106">NameParameterSet (Default)</span></span>
```
Get-AzureRmMapsAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c380f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c380f-107">InputObjectParameterSet</span></span>
```
Get-AzureRmMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c380f-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c380f-108">ResourceIdParameterSet</span></span>
```
Get-AzureRmMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c380f-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c380f-109">DESCRIPTION</span></span>
<span data-ttu-id="c380f-110">O cmdlet Get-AzureRmMapsAccountKey Obtém as chaves de API para uma conta provisionada do Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="c380f-110">The Get-AzureRmMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="c380f-111">Uma conta do Azure Maps tem duas chaves de API: primária e secundária.</span><span class="sxs-lookup"><span data-stu-id="c380f-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="c380f-112">As chaves permitem a interação com o ponto de extremidade da conta do Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="c380f-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="c380f-113">Use New-AzureRmMapsAccountKey (New-AzureRmMapsAccountKey. MD) para gerar novamente uma chave.</span><span class="sxs-lookup"><span data-stu-id="c380f-113">Use New-AzureRmMapsAccountKey (New-AzureRmMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="c380f-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c380f-114">EXAMPLES</span></span>

### <span data-ttu-id="c380f-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c380f-115">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="c380f-116">Retorna as chaves da conta chamada myaccount no grupo MyResource do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c380f-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="c380f-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c380f-117">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="c380f-118">Retorna as chaves da conta do Azure Maps especificada.</span><span class="sxs-lookup"><span data-stu-id="c380f-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="c380f-119">OS</span><span class="sxs-lookup"><span data-stu-id="c380f-119">PARAMETERS</span></span>

### <span data-ttu-id="c380f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c380f-120">-DefaultProfile</span></span>
<span data-ttu-id="c380f-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c380f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c380f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c380f-122">-InputObject</span></span>
<span data-ttu-id="c380f-123">Mapeia a conta canalizada do Get-AzureRmMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="c380f-123">Maps Account piped from Get-AzureRmMapsAccount.</span></span>

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

### <span data-ttu-id="c380f-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="c380f-124">-Name</span></span>
<span data-ttu-id="c380f-125">Mapeia o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="c380f-125">Maps Account Name.</span></span>

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

### <span data-ttu-id="c380f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c380f-126">-ResourceGroupName</span></span>
<span data-ttu-id="c380f-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c380f-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="c380f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c380f-128">-ResourceId</span></span>
<span data-ttu-id="c380f-129">Mapeia ResourceId de conta.</span><span class="sxs-lookup"><span data-stu-id="c380f-129">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="c380f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c380f-130">CommonParameters</span></span>
<span data-ttu-id="c380f-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c380f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c380f-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c380f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c380f-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c380f-133">INPUTS</span></span>

### <span data-ttu-id="c380f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c380f-134">System.String</span></span>

### <span data-ttu-id="c380f-135">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="c380f-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>
<span data-ttu-id="c380f-136">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c380f-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c380f-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c380f-137">OUTPUTS</span></span>

### <span data-ttu-id="c380f-138">Microsoft. Azure. Commands. Maps. Models. PSMapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c380f-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="c380f-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c380f-139">NOTES</span></span>

## <span data-ttu-id="c380f-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c380f-140">RELATED LINKS</span></span>
