---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: 833351c3abbf95eb898405f23241a20fe9affefa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114316"
---
# <span data-ttu-id="10836-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="10836-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="10836-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10836-102">SYNOPSIS</span></span>
<span data-ttu-id="10836-103">Cria uma nova Revisão de uma API existente.</span><span class="sxs-lookup"><span data-stu-id="10836-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="10836-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10836-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ApiRevisionDescription <String>] [-SourceApiRevision <String>] [-ServiceUrl <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10836-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="10836-105">DESCRIPTION</span></span>

<span data-ttu-id="10836-106">O cmdlet **New-AzApiManagementApiRevision** cria uma Revisão da API para uma API existente no contexto de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="10836-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="10836-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="10836-107">EXAMPLES</span></span>

### <span data-ttu-id="10836-108">Exemplo 1: Criar uma Revisão de API vazia para uma API</span><span class="sxs-lookup"><span data-stu-id="10836-108">Example 1: Create an empty API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"


New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"
```

<span data-ttu-id="10836-109">Esse comando cria uma Revisão da `2` `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="10836-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

### <span data-ttu-id="10836-110">Exemplo 2: Criar uma Revisão da API a partir de uma Api Existente e copiar Todas as operações, marcas e Políticas</span><span class="sxs-lookup"><span data-stu-id="10836-110">Example 2: Create an API Revision from an Existing Api and copy All operations, tags and Policies</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5" -SourceApiRevision "1" -ServiceUrl "https://echoapi.cloudapp.net/rev4"


ApiId                         : echo-api;rev=5
Name                          : Echo API
Description                   :
ServiceUrl                    : http://echoapi.cloudapp.net/api
Path                          : echo
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 5
ApiVersion                    :
IsCurrent                     : False
IsOnline                      : False
SubscriptionRequired          : True
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               :
Id                            : /subscriptions/subid/resourceGroups/apimService1/providers/Microsoft.ApiManagement/service/sdktestapim4163/apis/echo-api;rev=5
ResourceGroupName             : apimService1
ServiceName                   : sdktestapim4163
```

<span data-ttu-id="10836-111">Esse comando cria uma Revisão da `5` `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="10836-111">This command creates an API Revision `5` of the `echo-api` API.</span></span>

## <span data-ttu-id="10836-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10836-112">PARAMETERS</span></span>

### <span data-ttu-id="10836-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="10836-113">-ApiId</span></span>
<span data-ttu-id="10836-114">Identificador da API cuja Revisão deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="10836-114">Identifier for API whose Revision is to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10836-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="10836-115">-ApiRevision</span></span>
<span data-ttu-id="10836-116">Identificador de Revisão da Api.</span><span class="sxs-lookup"><span data-stu-id="10836-116">Revision Identifier of the Api.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10836-117">-ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="10836-117">-ApiRevisionDescription</span></span>
<span data-ttu-id="10836-118">Descrição da Revisão da Api.</span><span class="sxs-lookup"><span data-stu-id="10836-118">Api Revision Description.</span></span> <span data-ttu-id="10836-119">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="10836-119">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10836-120">-Contexto</span><span class="sxs-lookup"><span data-stu-id="10836-120">-Context</span></span>
<span data-ttu-id="10836-121">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="10836-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="10836-122">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="10836-122">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10836-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10836-123">-DefaultProfile</span></span>
<span data-ttu-id="10836-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="10836-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10836-125">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="10836-125">-ServiceUrl</span></span>
<span data-ttu-id="10836-126">Uma URL do serviço Web que expõe a API no serviço Backend.</span><span class="sxs-lookup"><span data-stu-id="10836-126">A URL of the web service exposing the API in the Backend service.</span></span> <span data-ttu-id="10836-127">Essa URL será usada apenas pelo Gerenciamento de API do Azure e não será pública.</span><span class="sxs-lookup"><span data-stu-id="10836-127">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="10836-128">Deve ter de 1 a 2000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="10836-128">Must be 1 to 2000 characters long.</span></span> <span data-ttu-id="10836-129">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="10836-129">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10836-130">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="10836-130">-SourceApiRevision</span></span>
<span data-ttu-id="10836-131">Identificador de Revisão de Api da API de origem.</span><span class="sxs-lookup"><span data-stu-id="10836-131">Api Revision identifier of the source API.</span></span> <span data-ttu-id="10836-132">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="10836-132">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10836-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="10836-133">-Confirm</span></span>
<span data-ttu-id="10836-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10836-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10836-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10836-135">-WhatIf</span></span>
<span data-ttu-id="10836-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="10836-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10836-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="10836-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10836-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10836-138">CommonParameters</span></span>
<span data-ttu-id="10836-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10836-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10836-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10836-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10836-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="10836-141">INPUTS</span></span>

### <span data-ttu-id="10836-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="10836-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="10836-143">System.String</span><span class="sxs-lookup"><span data-stu-id="10836-143">System.String</span></span>

## <span data-ttu-id="10836-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="10836-144">OUTPUTS</span></span>

### <span data-ttu-id="10836-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="10836-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="10836-146">Notas</span><span class="sxs-lookup"><span data-stu-id="10836-146">NOTES</span></span>

## <span data-ttu-id="10836-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10836-147">RELATED LINKS</span></span>

[<span data-ttu-id="10836-148">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="10836-148">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="10836-149">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="10836-149">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="10836-150">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="10836-150">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
