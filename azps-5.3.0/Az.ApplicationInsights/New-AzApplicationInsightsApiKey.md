---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 2afb8ebfa1305e736a226f48022f4c56ded2d809
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272059"
---
# <span data-ttu-id="eed2b-101">New-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="eed2b-101">New-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="eed2b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eed2b-102">SYNOPSIS</span></span>
<span data-ttu-id="eed2b-103">Criar uma chave de API do Application insights para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="eed2b-103">Create an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="eed2b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eed2b-104">SYNTAX</span></span>

### <span data-ttu-id="eed2b-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="eed2b-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eed2b-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eed2b-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eed2b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eed2b-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eed2b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eed2b-108">DESCRIPTION</span></span>
<span data-ttu-id="eed2b-109">Criar uma chave de API do Application insights para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="eed2b-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="eed2b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eed2b-110">EXAMPLES</span></span>

### <span data-ttu-id="eed2b-111">Exemplo 1 criar uma nova chave de API para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="eed2b-111">Example 1 Create a new Api Key for an application insights resource</span></span>
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

<span data-ttu-id="eed2b-112">Crie uma descrição da chave da API do Application insights como "testapiKey" com permissões "ReadTelemetry", "WriteAnnotations" para o recurso "teste" no grupo de recursos "Test Group".</span><span class="sxs-lookup"><span data-stu-id="eed2b-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="eed2b-113">OS</span><span class="sxs-lookup"><span data-stu-id="eed2b-113">PARAMETERS</span></span>

### <span data-ttu-id="eed2b-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="eed2b-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="eed2b-115">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="eed2b-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="eed2b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eed2b-116">-DefaultProfile</span></span>
<span data-ttu-id="eed2b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eed2b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eed2b-118">-Descrição</span><span class="sxs-lookup"><span data-stu-id="eed2b-118">-Description</span></span>
<span data-ttu-id="eed2b-119">Descrição para ajudar a identificar essa chave de API.</span><span class="sxs-lookup"><span data-stu-id="eed2b-119">Description to help identify this API key.</span></span>

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

### <span data-ttu-id="eed2b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="eed2b-120">-Name</span></span>
<span data-ttu-id="eed2b-121">Nome do componente.</span><span class="sxs-lookup"><span data-stu-id="eed2b-121">Component Name.</span></span>

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

### <span data-ttu-id="eed2b-122">-Permissões</span><span class="sxs-lookup"><span data-stu-id="eed2b-122">-Permissions</span></span>
<span data-ttu-id="eed2b-123">Permissões que a chave de API permite que os aplicativos façam.</span><span class="sxs-lookup"><span data-stu-id="eed2b-123">Permissions that API key allow apps to do.</span></span>

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

### <span data-ttu-id="eed2b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eed2b-124">-ResourceGroupName</span></span>
<span data-ttu-id="eed2b-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eed2b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="eed2b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eed2b-126">-ResourceId</span></span>
<span data-ttu-id="eed2b-127">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="eed2b-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="eed2b-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="eed2b-128">-Confirm</span></span>
<span data-ttu-id="eed2b-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eed2b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eed2b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eed2b-130">-WhatIf</span></span>
<span data-ttu-id="eed2b-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="eed2b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eed2b-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eed2b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eed2b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eed2b-133">CommonParameters</span></span>
<span data-ttu-id="eed2b-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eed2b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eed2b-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eed2b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eed2b-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eed2b-136">INPUTS</span></span>

### <span data-ttu-id="eed2b-137">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="eed2b-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="eed2b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="eed2b-138">System.String</span></span>

## <span data-ttu-id="eed2b-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eed2b-139">OUTPUTS</span></span>

### <span data-ttu-id="eed2b-140">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="eed2b-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="eed2b-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eed2b-141">NOTES</span></span>

## <span data-ttu-id="eed2b-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eed2b-142">RELATED LINKS</span></span>
