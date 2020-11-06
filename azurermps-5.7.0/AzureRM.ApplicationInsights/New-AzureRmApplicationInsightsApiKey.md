---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsApiKey.md
ms.openlocfilehash: 4c7f488e7a9ffca823128cccff18ba33b88dabfd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431744"
---
# <span data-ttu-id="0fb3a-101">New-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="0fb3a-101">New-AzureRmApplicationInsightsApiKey</span></span>

## <span data-ttu-id="0fb3a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0fb3a-102">SYNOPSIS</span></span>
<span data-ttu-id="0fb3a-103">Criar uma chave de API do Application insights para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="0fb3a-103">Create an application insights api key for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fb3a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0fb3a-104">SYNTAX</span></span>

### <span data-ttu-id="0fb3a-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0fb3a-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fb3a-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fb3a-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fb3a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fb3a-107">ResourceIdParameterSet</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fb3a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0fb3a-108">DESCRIPTION</span></span>
<span data-ttu-id="0fb3a-109">Criar uma chave de API do Application insights para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="0fb3a-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="0fb3a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0fb3a-110">EXAMPLES</span></span>

### <span data-ttu-id="0fb3a-111">Exemplo 1 criar uma nova chave de API para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="0fb3a-111">Example 1 Create a new Api Key for an application insights resource</span></span>
```
PS C:\>$apiKeyDescription="testapiKey"
PS C:\>$permissions = @("ReadTelemetry", "WriteAnnotations")
PS C:\>New-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test" -Description $apiKeyDescription -Permissions $permissions

ApiKey      : st0rfelw7m3oimfspozrtwgccxihiftbdwqjdfkg
CreatedDate : Fri, 27 Oct 2017 16:59:19 GMT
Id          : 1ed593f9-1561-4981-922d-6917971eecd3
Permissions : {ReadTelemetry, WriteAnnotations}
Description : testapiKey
```

<span data-ttu-id="0fb3a-112">Crie uma descrição da chave da API do Application insights como "testapiKey" com permissões "ReadTelemetry", "WriteAnnotations" para o recurso "teste" no grupo de recursos "Test Group".</span><span class="sxs-lookup"><span data-stu-id="0fb3a-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="0fb3a-113">OS</span><span class="sxs-lookup"><span data-stu-id="0fb3a-113">PARAMETERS</span></span>

### <span data-ttu-id="0fb3a-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="0fb3a-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="0fb3a-115">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="0fb3a-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="0fb3a-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0fb3a-116">-Confirm</span></span>
<span data-ttu-id="0fb3a-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fb3a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fb3a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fb3a-118">-DefaultProfile</span></span>
<span data-ttu-id="0fb3a-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0fb3a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fb3a-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="0fb3a-120">-Description</span></span>
<span data-ttu-id="0fb3a-121">Descrição para ajudar a identificar essa chave de API.</span><span class="sxs-lookup"><span data-stu-id="0fb3a-121">Description to help identify this API key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fb3a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="0fb3a-122">-Name</span></span>
<span data-ttu-id="0fb3a-123">Nome do componente.</span><span class="sxs-lookup"><span data-stu-id="0fb3a-123">Component Name.</span></span>

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

### <span data-ttu-id="0fb3a-124">-Permissões</span><span class="sxs-lookup"><span data-stu-id="0fb3a-124">-Permissions</span></span>
<span data-ttu-id="0fb3a-125">Permissões que a chave de API permite que os aplicativos façam.</span><span class="sxs-lookup"><span data-stu-id="0fb3a-125">Permissions that API key allow apps to do.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Accepted values: ReadTelemetry, WriteAnnotations, AuthenticateSDKControlChannel

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fb3a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fb3a-126">-ResourceGroupName</span></span>
<span data-ttu-id="0fb3a-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0fb3a-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="0fb3a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fb3a-128">-ResourceId</span></span>
<span data-ttu-id="0fb3a-129">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="0fb3a-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="0fb3a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fb3a-130">-WhatIf</span></span>
<span data-ttu-id="0fb3a-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0fb3a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0fb3a-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0fb3a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fb3a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fb3a-133">CommonParameters</span></span>
<span data-ttu-id="0fb3a-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fb3a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fb3a-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fb3a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fb3a-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0fb3a-136">INPUTS</span></span>

### <span data-ttu-id="0fb3a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0fb3a-137">System.String</span></span>
<span data-ttu-id="0fb3a-138">System. String []</span><span class="sxs-lookup"><span data-stu-id="0fb3a-138">System.String[]</span></span>

## <span data-ttu-id="0fb3a-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0fb3a-139">OUTPUTS</span></span>

### <span data-ttu-id="0fb3a-140">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="0fb3a-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="0fb3a-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0fb3a-141">NOTES</span></span>

## <span data-ttu-id="0fb3a-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0fb3a-142">RELATED LINKS</span></span>

