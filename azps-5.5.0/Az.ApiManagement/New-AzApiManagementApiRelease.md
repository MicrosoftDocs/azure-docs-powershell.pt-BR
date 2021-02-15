---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: 263e54adc39103a704dc4ea0bd30f396b5d00fc9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118064"
---
# <span data-ttu-id="c1dd6-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c1dd6-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="c1dd6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1dd6-102">SYNOPSIS</span></span>
<span data-ttu-id="c1dd6-103">Cria uma versão da API de uma revisão da API</span><span class="sxs-lookup"><span data-stu-id="c1dd6-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="c1dd6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1dd6-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1dd6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1dd6-105">DESCRIPTION</span></span>

<span data-ttu-id="c1dd6-106">O cmdlet **New-AzApiManagementApiRelease** cria uma Versão da API para uma Revisão da API no contexto de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="c1dd6-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span> <span data-ttu-id="c1dd6-107">Um Lançamento é usado para tornar a Revisão da Api como Revisão Atual.</span><span class="sxs-lookup"><span data-stu-id="c1dd6-107">A Release is used to make the Api Revision as Current Revision.</span></span>

## <span data-ttu-id="c1dd6-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c1dd6-108">EXAMPLES</span></span>

### <span data-ttu-id="c1dd6-109">Exemplo 1: Criar uma versão da API para uma revisão da API</span><span class="sxs-lookup"><span data-stu-id="c1dd6-109">Example 1: Create an API Release for an API Revision</span></span>
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

<span data-ttu-id="c1dd6-110">Este comando cria uma Versão de Revisão da API `2` do `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="c1dd6-110">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="c1dd6-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1dd6-111">PARAMETERS</span></span>

### <span data-ttu-id="c1dd6-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c1dd6-112">-ApiId</span></span>
<span data-ttu-id="c1dd6-113">Identificador da nova API.</span><span class="sxs-lookup"><span data-stu-id="c1dd6-113">Identifier for new API.</span></span>

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

### <span data-ttu-id="c1dd6-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="c1dd6-114">-ApiRevision</span></span>
<span data-ttu-id="c1dd6-115">Identificador da Revisão da Api.</span><span class="sxs-lookup"><span data-stu-id="c1dd6-115">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="c1dd6-116">-Contexto</span><span class="sxs-lookup"><span data-stu-id="c1dd6-116">-Context</span></span>
<span data-ttu-id="c1dd6-117">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c1dd6-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c1dd6-118">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="c1dd6-118">This parameter is required.</span></span>

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

### <span data-ttu-id="c1dd6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1dd6-119">-DefaultProfile</span></span>
<span data-ttu-id="c1dd6-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1dd6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1dd6-121">-Observação</span><span class="sxs-lookup"><span data-stu-id="c1dd6-121">-Note</span></span>
<span data-ttu-id="c1dd6-122">Notas de Versão da Api.</span><span class="sxs-lookup"><span data-stu-id="c1dd6-122">Api Release Notes.</span></span> <span data-ttu-id="c1dd6-123">Este parâmetro é opcional</span><span class="sxs-lookup"><span data-stu-id="c1dd6-123">This parameter is optional</span></span>

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

### <span data-ttu-id="c1dd6-124">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="c1dd6-124">-ReleaseId</span></span>
<span data-ttu-id="c1dd6-125">Identificador para o Lançamento da Api.</span><span class="sxs-lookup"><span data-stu-id="c1dd6-125">Identifier for the Api Release.</span></span>
<span data-ttu-id="c1dd6-126">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="c1dd6-126">This parameter is optional.</span></span>
<span data-ttu-id="c1dd6-127">Se não especificado, o identificador será gerado.</span><span class="sxs-lookup"><span data-stu-id="c1dd6-127">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="c1dd6-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c1dd6-128">-Confirm</span></span>
<span data-ttu-id="c1dd6-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1dd6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1dd6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1dd6-130">-WhatIf</span></span>
<span data-ttu-id="c1dd6-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c1dd6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1dd6-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c1dd6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1dd6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1dd6-133">CommonParameters</span></span>
<span data-ttu-id="c1dd6-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1dd6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1dd6-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1dd6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1dd6-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="c1dd6-136">INPUTS</span></span>

### <span data-ttu-id="c1dd6-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c1dd6-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c1dd6-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c1dd6-138">System.String</span></span>

## <span data-ttu-id="c1dd6-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="c1dd6-139">OUTPUTS</span></span>

### <span data-ttu-id="c1dd6-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c1dd6-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="c1dd6-141">Notas</span><span class="sxs-lookup"><span data-stu-id="c1dd6-141">NOTES</span></span>

## <span data-ttu-id="c1dd6-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1dd6-142">RELATED LINKS</span></span>

[<span data-ttu-id="c1dd6-143">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c1dd6-143">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="c1dd6-144">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c1dd6-144">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="c1dd6-145">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c1dd6-145">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)