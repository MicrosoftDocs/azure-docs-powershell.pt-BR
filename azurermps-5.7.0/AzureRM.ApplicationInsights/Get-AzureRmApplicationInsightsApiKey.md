---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/get-azurermapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsApiKey.md
ms.openlocfilehash: 705ebfc151ef4f6bcd5029026ce08ee1da5bd676
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431749"
---
# <span data-ttu-id="364c6-101">Get-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="364c6-101">Get-AzureRmApplicationInsightsApiKey</span></span>

## <span data-ttu-id="364c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="364c6-102">SYNOPSIS</span></span>
<span data-ttu-id="364c6-103">Obter as chaves de API do Application insights para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="364c6-103">Get application insights api keys for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="364c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="364c6-104">SYNTAX</span></span>

### <span data-ttu-id="364c6-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="364c6-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="364c6-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="364c6-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ApiKeyId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="364c6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="364c6-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmApplicationInsightsApiKey [-ResourceId] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="364c6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="364c6-108">DESCRIPTION</span></span>
<span data-ttu-id="364c6-109">Obter as chaves de API do Application insights para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="364c6-109">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="364c6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="364c6-110">EXAMPLES</span></span>

### <span data-ttu-id="364c6-111">Exemplo 1 obter as chaves de API para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="364c6-111">Example 1 Get Api Keys for an application insights resource</span></span>
```
PS C:\>  Get-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"

Id                                   Description Permissions                       CreatedDate                   ApiKey
--                                   ----------- -----------                       -----------                   ------
7c4c61dc-b392-4aa4-992f-ee92b84e5dee test1 ReadTelemetry                     Wed, 18 Oct 2017 23:36:40 GMT
63657030-dea6-4c52-82f4-6f5128cb92cb test2  {ReadTelemetry, WriteAnnotations} Wed, 18 Oct 2017 21:46:41 GMT
82549f39-f3ae-492e-8f94-f7aada75fa57 test3  ReadTelemetry                     Wed, 18 Oct 2017 22:30:23 GMT
```

<span data-ttu-id="364c6-112">Obter as chaves de API do Application insights para o recurso "teste" no grupo de recursos "grupo de teste".</span><span class="sxs-lookup"><span data-stu-id="364c6-112">Get application insights api keys for resource "test" in resource group "testGroup".</span></span>

### <span data-ttu-id="364c6-113">Exemplo 2 obter chave de API específica para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="364c6-113">Example 2 Get specific API key for an application insights resource</span></span>
```
PS C:\>  Get-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId 
7c4c61dc-b392-4aa4-992f-ee92b84e5dee
ApiKey      :
CreatedDate : Wed, 18 Oct 2017 23:36:40 GMT
Id          : 7c4c61dc-b392-4aa4-992f-ee92b84e5dee
Permissions : {ReadTelemetry}
Description : test1
```

<span data-ttu-id="364c6-114">Obtenha a chave de API específica do Application insights que ID é "dd173f38-4fd1-4C75-8af5-9 9c29aa0f867" para o recurso "teste" no grupo de recursos "Test Group".</span><span class="sxs-lookup"><span data-stu-id="364c6-114">Get specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="364c6-115">OS</span><span class="sxs-lookup"><span data-stu-id="364c6-115">PARAMETERS</span></span>

### <span data-ttu-id="364c6-116">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="364c6-116">-ApiKeyId</span></span>
<span data-ttu-id="364c6-117">ID da chave de API do Application insights.</span><span class="sxs-lookup"><span data-stu-id="364c6-117">Application Insights Api Key Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="364c6-118">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="364c6-118">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="364c6-119">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="364c6-119">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="364c6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="364c6-120">-DefaultProfile</span></span>
<span data-ttu-id="364c6-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="364c6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="364c6-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="364c6-122">-Name</span></span>
<span data-ttu-id="364c6-123">Nome do componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="364c6-123">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="364c6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="364c6-124">-ResourceGroupName</span></span>
<span data-ttu-id="364c6-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="364c6-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="364c6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="364c6-126">-ResourceId</span></span>
<span data-ttu-id="364c6-127">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="364c6-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="364c6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="364c6-128">CommonParameters</span></span>
<span data-ttu-id="364c6-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="364c6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="364c6-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="364c6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="364c6-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="364c6-131">INPUTS</span></span>

### <span data-ttu-id="364c6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="364c6-132">System.String</span></span>

## <span data-ttu-id="364c6-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="364c6-133">OUTPUTS</span></span>

### <span data-ttu-id="364c6-134">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="364c6-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="364c6-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="364c6-135">NOTES</span></span>

## <span data-ttu-id="364c6-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="364c6-136">RELATED LINKS</span></span>

