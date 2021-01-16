---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: 263e54adc39103a704dc4ea0bd30f396b5d00fc9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258671"
---
# <span data-ttu-id="a1bca-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a1bca-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="a1bca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1bca-102">SYNOPSIS</span></span>
<span data-ttu-id="a1bca-103">Cria uma versão de API de uma revisão de API</span><span class="sxs-lookup"><span data-stu-id="a1bca-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="a1bca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1bca-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1bca-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1bca-105">DESCRIPTION</span></span>

<span data-ttu-id="a1bca-106">O cmdlet **New-AzApiManagementApiRelease** cria uma versão de API para uma revisão de API no contexto de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="a1bca-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span> <span data-ttu-id="a1bca-107">Uma versão é usada para fazer com que a revisão da API seja a revisão atual.</span><span class="sxs-lookup"><span data-stu-id="a1bca-107">A Release is used to make the Api Revision as Current Revision.</span></span>

## <span data-ttu-id="a1bca-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1bca-108">EXAMPLES</span></span>

### <span data-ttu-id="a1bca-109">Exemplo 1: criar uma versão de API para uma revisão de API</span><span class="sxs-lookup"><span data-stu-id="a1bca-109">Example 1: Create an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRelease -Context $context  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6 -Note "Releasing version 6"


ReleaseId         : 7e4d3fbb43c146c4bf406499ef9411f4
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 1:16:29 AM
UpdatedDateTime   : 5/17/2018 1:16:29 AM
Notes             : Releasing version 6
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/7e4d3fbb43c146c4bf40649
                    9ef9411f4
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="a1bca-110">Esse comando cria uma versão de API da revisão `2` do `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="a1bca-110">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="a1bca-111">OS</span><span class="sxs-lookup"><span data-stu-id="a1bca-111">PARAMETERS</span></span>

### <span data-ttu-id="a1bca-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a1bca-112">-ApiId</span></span>
<span data-ttu-id="a1bca-113">Identificador para a nova API.</span><span class="sxs-lookup"><span data-stu-id="a1bca-113">Identifier for new API.</span></span>

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

### <span data-ttu-id="a1bca-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="a1bca-114">-ApiRevision</span></span>
<span data-ttu-id="a1bca-115">Identificador da revisão da API.</span><span class="sxs-lookup"><span data-stu-id="a1bca-115">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="a1bca-116">-Contexto</span><span class="sxs-lookup"><span data-stu-id="a1bca-116">-Context</span></span>
<span data-ttu-id="a1bca-117">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a1bca-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a1bca-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a1bca-118">This parameter is required.</span></span>

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

### <span data-ttu-id="a1bca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1bca-119">-DefaultProfile</span></span>
<span data-ttu-id="a1bca-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1bca-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1bca-121">-Nota</span><span class="sxs-lookup"><span data-stu-id="a1bca-121">-Note</span></span>
<span data-ttu-id="a1bca-122">Notas de versão da API.</span><span class="sxs-lookup"><span data-stu-id="a1bca-122">Api Release Notes.</span></span> <span data-ttu-id="a1bca-123">Este parâmetro é opcional</span><span class="sxs-lookup"><span data-stu-id="a1bca-123">This parameter is optional</span></span>

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

### <span data-ttu-id="a1bca-124">-Rereleaseid</span><span class="sxs-lookup"><span data-stu-id="a1bca-124">-ReleaseId</span></span>
<span data-ttu-id="a1bca-125">Identificador para a versão da API.</span><span class="sxs-lookup"><span data-stu-id="a1bca-125">Identifier for the Api Release.</span></span>
<span data-ttu-id="a1bca-126">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a1bca-126">This parameter is optional.</span></span>
<span data-ttu-id="a1bca-127">Se não for gerado um identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="a1bca-127">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="a1bca-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a1bca-128">-Confirm</span></span>
<span data-ttu-id="a1bca-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1bca-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1bca-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1bca-130">-WhatIf</span></span>
<span data-ttu-id="a1bca-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a1bca-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1bca-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a1bca-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1bca-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1bca-133">CommonParameters</span></span>
<span data-ttu-id="a1bca-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1bca-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1bca-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1bca-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1bca-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1bca-136">INPUTS</span></span>

### <span data-ttu-id="a1bca-137">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a1bca-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a1bca-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a1bca-138">System.String</span></span>

## <span data-ttu-id="a1bca-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1bca-139">OUTPUTS</span></span>

### <span data-ttu-id="a1bca-140">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a1bca-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="a1bca-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1bca-141">NOTES</span></span>

## <span data-ttu-id="a1bca-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1bca-142">RELATED LINKS</span></span>

[<span data-ttu-id="a1bca-143">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a1bca-143">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="a1bca-144">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a1bca-144">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="a1bca-145">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a1bca-145">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)