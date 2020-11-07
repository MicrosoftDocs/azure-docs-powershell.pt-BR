---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
ms.openlocfilehash: bf5051f22d06e9e248501ecfb602bd47d3faaf39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771315"
---
# <span data-ttu-id="0e975-101">Get-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="0e975-101">Get-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="0e975-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e975-102">SYNOPSIS</span></span>
<span data-ttu-id="0e975-103">Obter as chaves de API do Application insights para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="0e975-103">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="0e975-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e975-104">SYNTAX</span></span>

### <span data-ttu-id="0e975-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0e975-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e975-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e975-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ApiKeyId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e975-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e975-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceId] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e975-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0e975-108">DESCRIPTION</span></span>
<span data-ttu-id="0e975-109">Obter as chaves de API do Application insights para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="0e975-109">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="0e975-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0e975-110">EXAMPLES</span></span>

### <span data-ttu-id="0e975-111">Exemplo 1 obter as chaves de API para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="0e975-111">Example 1 Get Api Keys for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"

Id                                   Description Permissions                       CreatedDate                   ApiKey
--                                   ----------- -----------                       -----------                   ------
7c4c61dc-b392-4aa4-992f-ee92b84e5dee test1 ReadTelemetry                     Wed, 18 Oct 2017 23:36:40 GMT
63657030-dea6-4c52-82f4-6f5128cb92cb test2  {ReadTelemetry, WriteAnnotations} Wed, 18 Oct 2017 21:46:41 GMT
82549f39-f3ae-492e-8f94-f7aada75fa57 test3  ReadTelemetry                     Wed, 18 Oct 2017 22:30:23 GMT
```

<span data-ttu-id="0e975-112">Obter as chaves de API do Application insights para o recurso "teste" no grupo de recursos "grupo de teste".</span><span class="sxs-lookup"><span data-stu-id="0e975-112">Get application insights api keys for resource "test" in resource group "testGroup".</span></span>

### <span data-ttu-id="0e975-113">Exemplo 2 obter chave de API específica para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="0e975-113">Example 2 Get specific API key for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId 
7c4c61dc-b392-4aa4-992f-ee92b84e5dee
ApiKey      :
CreatedDate : Wed, 18 Oct 2017 23:36:40 GMT
Id          : 7c4c61dc-b392-4aa4-992f-ee92b84e5dee
Permissions : {ReadTelemetry}
Description : test1
```

<span data-ttu-id="0e975-114">Obtenha a chave de API específica do Application insights que ID é "dd173f38-4fd1-4C75-8af5-9 9c29aa0f867" para o recurso "teste" no grupo de recursos "Test Group".</span><span class="sxs-lookup"><span data-stu-id="0e975-114">Get specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="0e975-115">OS</span><span class="sxs-lookup"><span data-stu-id="0e975-115">PARAMETERS</span></span>

### <span data-ttu-id="0e975-116">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="0e975-116">-ApiKeyId</span></span>
<span data-ttu-id="0e975-117">ID da chave de API do Application insights.</span><span class="sxs-lookup"><span data-stu-id="0e975-117">Application Insights Api Key Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e975-118">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="0e975-118">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="0e975-119">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="0e975-119">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e975-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e975-120">-DefaultProfile</span></span>
<span data-ttu-id="0e975-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0e975-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e975-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e975-122">-Name</span></span>
<span data-ttu-id="0e975-123">Nome do componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="0e975-123">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e975-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e975-124">-ResourceGroupName</span></span>
<span data-ttu-id="0e975-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0e975-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e975-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e975-126">-ResourceId</span></span>
<span data-ttu-id="0e975-127">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="0e975-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="0e975-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e975-128">CommonParameters</span></span>
<span data-ttu-id="0e975-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e975-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e975-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e975-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e975-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0e975-131">INPUTS</span></span>

### <span data-ttu-id="0e975-132">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="0e975-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="0e975-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0e975-133">System.String</span></span>

## <span data-ttu-id="0e975-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0e975-134">OUTPUTS</span></span>

### <span data-ttu-id="0e975-135">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="0e975-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="0e975-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0e975-136">NOTES</span></span>

## <span data-ttu-id="0e975-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e975-137">RELATED LINKS</span></span>
