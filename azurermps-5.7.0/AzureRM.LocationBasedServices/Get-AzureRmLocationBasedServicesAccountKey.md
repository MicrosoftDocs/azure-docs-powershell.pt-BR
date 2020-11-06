---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/get-azurermlocationbasedservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccountKey.md
ms.openlocfilehash: 1f528bb0a80f039b9a2be7cb4cb6e4c7fbc740c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440852"
---
# <span data-ttu-id="9c792-101">Get-AzureRmLocationBasedServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="9c792-101">Get-AzureRmLocationBasedServicesAccountKey</span></span>

## <span data-ttu-id="9c792-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c792-102">SYNOPSIS</span></span>
<span data-ttu-id="9c792-103">Obtém as chaves de API para uma conta.</span><span class="sxs-lookup"><span data-stu-id="9c792-103">Gets the API keys for an account.</span></span> <span data-ttu-id="9c792-104">Essas chaves são o mecanismo de autenticação usado em chamadas subsequentes para serviços baseados no Azure Location.</span><span class="sxs-lookup"><span data-stu-id="9c792-104">These keys are the authentication mechanism used in subsequent calls to Azure Location Based Services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c792-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c792-105">SYNTAX</span></span>

### <span data-ttu-id="9c792-106">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9c792-106">NameParameterSet (Default)</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c792-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c792-107">InputObjectParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c792-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c792-108">ResourceIdParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c792-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c792-109">DESCRIPTION</span></span>
<span data-ttu-id="9c792-110">O cmdlet **Get-AzureRmLocationBasedServicesAccountKey** Obtém as chaves de API para uma conta de serviços com base em um local provisionado.</span><span class="sxs-lookup"><span data-stu-id="9c792-110">The **Get-AzureRmLocationBasedServicesAccountKey** cmdlet gets the API keys for a provisioned Location Based Services account.</span></span>

<span data-ttu-id="9c792-111">Uma conta de serviços com base em local tem duas chaves de API: primária e secundária.</span><span class="sxs-lookup"><span data-stu-id="9c792-111">A Location Based Services account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="9c792-112">As chaves permitem a interação com o ponto de extremidade da conta de serviços baseado em local.</span><span class="sxs-lookup"><span data-stu-id="9c792-112">The keys enable interaction with the Location Based Services account endpoint.</span></span>

<span data-ttu-id="9c792-113">Use [New-AzureRmLocationBasedServicesAccountKey](New-AzureRmLocationBasedServicesAccountKey.md) para gerar novamente uma chave.</span><span class="sxs-lookup"><span data-stu-id="9c792-113">Use [New-AzureRmLocationBasedServicesAccountKey](New-AzureRmLocationBasedServicesAccountKey.md) to regenerate a key.</span></span>

## <span data-ttu-id="9c792-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c792-114">EXAMPLES</span></span>

### <span data-ttu-id="9c792-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9c792-115">Example 1</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="9c792-116">Retorna as chaves da conta chamada myaccount no grupo MyResource do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9c792-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="9c792-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9c792-117">Example 2</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="9c792-118">Retorna as chaves da conta de serviços com base em local especificada.</span><span class="sxs-lookup"><span data-stu-id="9c792-118">Returns the keys for the specified Location Based Services Account.</span></span>

## <span data-ttu-id="9c792-119">OS</span><span class="sxs-lookup"><span data-stu-id="9c792-119">PARAMETERS</span></span>

### <span data-ttu-id="9c792-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c792-120">-DefaultProfile</span></span>
<span data-ttu-id="9c792-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c792-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c792-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c792-122">-InputObject</span></span>
<span data-ttu-id="9c792-123">Conta de serviços baseados em localização canalizada do [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span><span class="sxs-lookup"><span data-stu-id="9c792-123">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

```yaml
Type: PSLocationBasedServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c792-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c792-124">-Name</span></span>
<span data-ttu-id="9c792-125">Nome da conta de serviços baseados em local.</span><span class="sxs-lookup"><span data-stu-id="9c792-125">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c792-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c792-126">-ResourceGroupName</span></span>
<span data-ttu-id="9c792-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9c792-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c792-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c792-128">-ResourceId</span></span>
<span data-ttu-id="9c792-129">Resource Resource da conta de serviços baseados em local.</span><span class="sxs-lookup"><span data-stu-id="9c792-129">Location Based Services Account ResourceId.</span></span>
```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c792-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c792-130">CommonParameters</span></span>
<span data-ttu-id="9c792-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c792-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c792-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c792-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c792-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c792-133">INPUTS</span></span>

### <span data-ttu-id="9c792-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9c792-134">System.String</span></span>

## <span data-ttu-id="9c792-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c792-135">OUTPUTS</span></span>

### <span data-ttu-id="9c792-136">Microsoft. Azure. Commands. LocationBasedServices. Models. PSLocationBasedServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9c792-136">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccountKeys</span></span>

### <span data-ttu-id="9c792-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c792-137">CommonParameters</span></span>
<span data-ttu-id="9c792-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c792-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c792-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c792-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c792-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c792-140">NOTES</span></span>

## <span data-ttu-id="9c792-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c792-141">RELATED LINKS</span></span>
