---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsApiKey.md
ms.openlocfilehash: 7fbf269b43868724b015bd087536c49ccce71f73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432985"
---
# <span data-ttu-id="fc55b-101">Remove-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="fc55b-101">Remove-AzureRmApplicationInsightsApiKey</span></span>

## <span data-ttu-id="fc55b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc55b-102">SYNOPSIS</span></span>
<span data-ttu-id="fc55b-103">Remover uma chave de API do Application insights para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="fc55b-103">Remove an application insights api key for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc55b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc55b-104">SYNTAX</span></span>

### <span data-ttu-id="fc55b-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fc55b-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc55b-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc55b-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc55b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc55b-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc55b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc55b-108">DESCRIPTION</span></span>
<span data-ttu-id="fc55b-109">Remover uma chave de API do Application insights para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="fc55b-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="fc55b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc55b-110">EXAMPLES</span></span>

### <span data-ttu-id="fc55b-111">Exemplo 1 remover uma chave de API do Application insights para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="fc55b-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Get-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="fc55b-112">Remova a chave de API específica do Application insights que ID é "dd173f38-4fd1-4C75-8af5-9 9c29aa0f867" para o recurso "teste" no grupo de recursos "Test Group".</span><span class="sxs-lookup"><span data-stu-id="fc55b-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="fc55b-113">OS</span><span class="sxs-lookup"><span data-stu-id="fc55b-113">PARAMETERS</span></span>

### <span data-ttu-id="fc55b-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="fc55b-114">-ApiKeyId</span></span>
<span data-ttu-id="fc55b-115">ID da chave de API do Application insights.</span><span class="sxs-lookup"><span data-stu-id="fc55b-115">Application Insights API Key ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc55b-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="fc55b-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="fc55b-117">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="fc55b-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="fc55b-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fc55b-118">-Confirm</span></span>
<span data-ttu-id="fc55b-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc55b-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc55b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc55b-120">-DefaultProfile</span></span>
<span data-ttu-id="fc55b-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fc55b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc55b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc55b-122">-Name</span></span>
<span data-ttu-id="fc55b-123">Nome do componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="fc55b-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="fc55b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc55b-124">-PassThru</span></span>
<span data-ttu-id="fc55b-125">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fc55b-125">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="fc55b-126">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="fc55b-126">This parameter is optional.</span></span> <span data-ttu-id="fc55b-127">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="fc55b-127">Default value is false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc55b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc55b-128">-ResourceGroupName</span></span>
<span data-ttu-id="fc55b-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fc55b-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="fc55b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc55b-130">-ResourceId</span></span>
<span data-ttu-id="fc55b-131">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="fc55b-131">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="fc55b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc55b-132">-WhatIf</span></span>
<span data-ttu-id="fc55b-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fc55b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc55b-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fc55b-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc55b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc55b-135">CommonParameters</span></span>
<span data-ttu-id="fc55b-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc55b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc55b-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc55b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc55b-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc55b-138">INPUTS</span></span>

### <span data-ttu-id="fc55b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fc55b-139">System.String</span></span>

## <span data-ttu-id="fc55b-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc55b-140">OUTPUTS</span></span>

### <span data-ttu-id="fc55b-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="fc55b-141">System.Object</span></span>

## <span data-ttu-id="fc55b-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc55b-142">NOTES</span></span>

## <span data-ttu-id="fc55b-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc55b-143">RELATED LINKS</span></span>

