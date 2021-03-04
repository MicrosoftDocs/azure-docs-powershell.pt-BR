---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/new-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 0137a349408234f31f0002849230e023c0544f68
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889819"
---
# <span data-ttu-id="c1e7a-101">New-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="c1e7a-101">New-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="c1e7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="c1e7a-103">Criar uma chave de api de insights de aplicativo para um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c1e7a-103">Create an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="c1e7a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c1e7a-104">SYNTAX</span></span>

### <span data-ttu-id="c1e7a-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c1e7a-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1e7a-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1e7a-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1e7a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1e7a-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1e7a-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c1e7a-108">DESCRIPTION</span></span>
<span data-ttu-id="c1e7a-109">Criar chaves de api de insights de aplicativo para um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c1e7a-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="c1e7a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1e7a-110">EXAMPLES</span></span>

### <span data-ttu-id="c1e7a-111">Exemplo 1 Criar uma nova Chave de Api para um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c1e7a-111">Example 1 Create a new Api Key for an application insights resource</span></span>
```
PS C:\>$apiKeyDescription="testapiKey"
PS C:\>$permissions = @("ReadTelemetry", "WriteAnnotations")
PS C:\>New-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test" -Description $apiKeyDescription -Permissions $permissions

ApiKey      : st0rfelw7m3oimfspozrtwgccxihiftbdwqjdfkg
CreatedDate : Fri, 27 Oct 2017 16:59:19 GMT
Id          : 1ed593f9-1561-4981-922d-6917971eecd3
Permissions : {ReadTelemetry, WriteAnnotations}
Description : testapiKey
```

<span data-ttu-id="c1e7a-112">Crie a descrição da chave da api de insights do aplicativo como "testapiKey" com permissões "ReadTelemetry", "WriteAnnotations" para o recurso "test" no grupo de recursos "testGroup".</span><span class="sxs-lookup"><span data-stu-id="c1e7a-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="c1e7a-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c1e7a-113">PARAMETERS</span></span>

### <span data-ttu-id="c1e7a-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c1e7a-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="c1e7a-115">Objeto Application Insights Component.</span><span class="sxs-lookup"><span data-stu-id="c1e7a-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="c1e7a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1e7a-116">-DefaultProfile</span></span>
<span data-ttu-id="c1e7a-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c1e7a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1e7a-118">-Description</span><span class="sxs-lookup"><span data-stu-id="c1e7a-118">-Description</span></span>
<span data-ttu-id="c1e7a-119">Descrição para ajudar a identificar essa chave de API.</span><span class="sxs-lookup"><span data-stu-id="c1e7a-119">Description to help identify this API key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e7a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c1e7a-120">-Name</span></span>
<span data-ttu-id="c1e7a-121">Nome do componente.</span><span class="sxs-lookup"><span data-stu-id="c1e7a-121">Component Name.</span></span>

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

### <span data-ttu-id="c1e7a-122">-Permissões</span><span class="sxs-lookup"><span data-stu-id="c1e7a-122">-Permissions</span></span>
<span data-ttu-id="c1e7a-123">Permissões que a chave da API permitem que os aplicativos faça.</span><span class="sxs-lookup"><span data-stu-id="c1e7a-123">Permissions that API key allow apps to do.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ReadTelemetry, WriteAnnotations, AuthenticateSDKControlChannel

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e7a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1e7a-124">-ResourceGroupName</span></span>
<span data-ttu-id="c1e7a-125">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="c1e7a-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c1e7a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1e7a-126">-ResourceId</span></span>
<span data-ttu-id="c1e7a-127">ID do Recurso de Componente do Application Insights.</span><span class="sxs-lookup"><span data-stu-id="c1e7a-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="c1e7a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1e7a-128">-Confirm</span></span>
<span data-ttu-id="c1e7a-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1e7a-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e7a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1e7a-130">-WhatIf</span></span>
<span data-ttu-id="c1e7a-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c1e7a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1e7a-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c1e7a-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e7a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1e7a-133">CommonParameters</span></span>
<span data-ttu-id="c1e7a-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1e7a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1e7a-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1e7a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1e7a-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1e7a-136">INPUTS</span></span>

### <span data-ttu-id="c1e7a-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c1e7a-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="c1e7a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c1e7a-138">System.String</span></span>

## <span data-ttu-id="c1e7a-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c1e7a-139">OUTPUTS</span></span>

### <span data-ttu-id="c1e7a-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span><span class="sxs-lookup"><span data-stu-id="c1e7a-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="c1e7a-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="c1e7a-141">NOTES</span></span>

## <span data-ttu-id="c1e7a-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1e7a-142">RELATED LINKS</span></span>
