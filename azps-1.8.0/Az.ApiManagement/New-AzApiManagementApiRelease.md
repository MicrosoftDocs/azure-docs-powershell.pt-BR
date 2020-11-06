---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: f816488e6334c0e9c410bb1c24f46501a1fefe85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595647"
---
# <span data-ttu-id="25afe-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="25afe-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="25afe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25afe-102">SYNOPSIS</span></span>
<span data-ttu-id="25afe-103">Cria uma versão de API de uma revisão de API</span><span class="sxs-lookup"><span data-stu-id="25afe-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="25afe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25afe-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25afe-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25afe-105">DESCRIPTION</span></span>

<span data-ttu-id="25afe-106">O cmdlet **New-AzApiManagementApiRelease** cria uma versão de API para uma revisão de API no contexto de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="25afe-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span>

## <span data-ttu-id="25afe-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25afe-107">EXAMPLES</span></span>

### <span data-ttu-id="25afe-108">Exemplo 1: criar uma versão de API para uma revisão de API</span><span class="sxs-lookup"><span data-stu-id="25afe-108">Example 1: Create an API Release for an API Revision</span></span>
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

<span data-ttu-id="25afe-109">Esse comando cria uma versão de API da revisão `2` do `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="25afe-109">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="25afe-110">OS</span><span class="sxs-lookup"><span data-stu-id="25afe-110">PARAMETERS</span></span>

### <span data-ttu-id="25afe-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="25afe-111">-ApiId</span></span>
<span data-ttu-id="25afe-112">Identificador para a nova API.</span><span class="sxs-lookup"><span data-stu-id="25afe-112">Identifier for new API.</span></span>

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

### <span data-ttu-id="25afe-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="25afe-113">-ApiRevision</span></span>
<span data-ttu-id="25afe-114">Identificador da revisão da API.</span><span class="sxs-lookup"><span data-stu-id="25afe-114">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="25afe-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="25afe-115">-Context</span></span>
<span data-ttu-id="25afe-116">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="25afe-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="25afe-117">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="25afe-117">This parameter is required.</span></span>

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

### <span data-ttu-id="25afe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25afe-118">-DefaultProfile</span></span>
<span data-ttu-id="25afe-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25afe-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25afe-120">-Nota</span><span class="sxs-lookup"><span data-stu-id="25afe-120">-Note</span></span>
<span data-ttu-id="25afe-121">Notas de versão da API.</span><span class="sxs-lookup"><span data-stu-id="25afe-121">Api Release Notes.</span></span> <span data-ttu-id="25afe-122">Este parâmetro é opcional</span><span class="sxs-lookup"><span data-stu-id="25afe-122">This parameter is optional</span></span>

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

### <span data-ttu-id="25afe-123">-Rereleaseid</span><span class="sxs-lookup"><span data-stu-id="25afe-123">-ReleaseId</span></span>
<span data-ttu-id="25afe-124">Identificador para a versão da API.</span><span class="sxs-lookup"><span data-stu-id="25afe-124">Identifier for the Api Release.</span></span>
<span data-ttu-id="25afe-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="25afe-125">This parameter is optional.</span></span>
<span data-ttu-id="25afe-126">Se não for gerado um identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="25afe-126">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="25afe-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="25afe-127">-Confirm</span></span>
<span data-ttu-id="25afe-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25afe-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25afe-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25afe-129">-WhatIf</span></span>
<span data-ttu-id="25afe-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="25afe-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25afe-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="25afe-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25afe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25afe-132">CommonParameters</span></span>
<span data-ttu-id="25afe-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25afe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25afe-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25afe-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25afe-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25afe-135">INPUTS</span></span>

### <span data-ttu-id="25afe-136">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="25afe-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="25afe-137">System. String</span><span class="sxs-lookup"><span data-stu-id="25afe-137">System.String</span></span>

## <span data-ttu-id="25afe-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25afe-138">OUTPUTS</span></span>

### <span data-ttu-id="25afe-139">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="25afe-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="25afe-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25afe-140">NOTES</span></span>

## <span data-ttu-id="25afe-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25afe-141">RELATED LINKS</span></span>

[<span data-ttu-id="25afe-142">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="25afe-142">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="25afe-143">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="25afe-143">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="25afe-144">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="25afe-144">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)