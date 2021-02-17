---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: 5e536d3174a9a71cf4f648172f3d06e6fc5ae79f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400988"
---
# <span data-ttu-id="1f379-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="1f379-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="1f379-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f379-102">SYNOPSIS</span></span>
<span data-ttu-id="1f379-103">Cria uma versão da API de uma revisão da API</span><span class="sxs-lookup"><span data-stu-id="1f379-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="1f379-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f379-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f379-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f379-105">DESCRIPTION</span></span>

<span data-ttu-id="1f379-106">O cmdlet **New-AzApiManagementApiRelease** cria uma Versão da API para uma Revisão da API no contexto de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="1f379-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span>

## <span data-ttu-id="1f379-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1f379-107">EXAMPLES</span></span>

### <span data-ttu-id="1f379-108">Exemplo 1: Criar uma versão da API para uma revisão da API</span><span class="sxs-lookup"><span data-stu-id="1f379-108">Example 1: Create an API Release for an API Revision</span></span>
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

<span data-ttu-id="1f379-109">Este comando cria uma Versão de Revisão da API `2` do `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="1f379-109">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="1f379-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f379-110">PARAMETERS</span></span>

### <span data-ttu-id="1f379-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="1f379-111">-ApiId</span></span>
<span data-ttu-id="1f379-112">Identificador da nova API.</span><span class="sxs-lookup"><span data-stu-id="1f379-112">Identifier for new API.</span></span>

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

### <span data-ttu-id="1f379-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="1f379-113">-ApiRevision</span></span>
<span data-ttu-id="1f379-114">Identificador da Revisão da Api.</span><span class="sxs-lookup"><span data-stu-id="1f379-114">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="1f379-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="1f379-115">-Context</span></span>
<span data-ttu-id="1f379-116">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1f379-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1f379-117">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="1f379-117">This parameter is required.</span></span>

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

### <span data-ttu-id="1f379-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f379-118">-DefaultProfile</span></span>
<span data-ttu-id="1f379-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f379-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f379-120">-Observação</span><span class="sxs-lookup"><span data-stu-id="1f379-120">-Note</span></span>
<span data-ttu-id="1f379-121">Notas de Versão da Api.</span><span class="sxs-lookup"><span data-stu-id="1f379-121">Api Release Notes.</span></span> <span data-ttu-id="1f379-122">Este parâmetro é opcional</span><span class="sxs-lookup"><span data-stu-id="1f379-122">This parameter is optional</span></span>

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

### <span data-ttu-id="1f379-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="1f379-123">-ReleaseId</span></span>
<span data-ttu-id="1f379-124">Identificador para o Lançamento da Api.</span><span class="sxs-lookup"><span data-stu-id="1f379-124">Identifier for the Api Release.</span></span>
<span data-ttu-id="1f379-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="1f379-125">This parameter is optional.</span></span>
<span data-ttu-id="1f379-126">Se não especificado, o identificador será gerado.</span><span class="sxs-lookup"><span data-stu-id="1f379-126">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="1f379-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1f379-127">-Confirm</span></span>
<span data-ttu-id="1f379-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f379-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f379-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f379-129">-WhatIf</span></span>
<span data-ttu-id="1f379-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1f379-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f379-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1f379-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f379-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f379-132">CommonParameters</span></span>
<span data-ttu-id="1f379-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f379-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f379-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f379-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f379-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="1f379-135">INPUTS</span></span>

### <span data-ttu-id="1f379-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1f379-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1f379-137">System.String</span><span class="sxs-lookup"><span data-stu-id="1f379-137">System.String</span></span>

## <span data-ttu-id="1f379-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="1f379-138">OUTPUTS</span></span>

### <span data-ttu-id="1f379-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="1f379-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="1f379-140">Notas</span><span class="sxs-lookup"><span data-stu-id="1f379-140">NOTES</span></span>

## <span data-ttu-id="1f379-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f379-141">RELATED LINKS</span></span>

[<span data-ttu-id="1f379-142">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="1f379-142">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="1f379-143">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="1f379-143">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="1f379-144">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="1f379-144">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)