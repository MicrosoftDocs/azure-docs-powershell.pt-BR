---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
ms.openlocfilehash: 9673df14bdd0f5b7d0e946170a155231e8c4e751
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412649"
---
# <span data-ttu-id="52a9b-101">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="52a9b-101">Remove-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="52a9b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52a9b-102">SYNOPSIS</span></span>
<span data-ttu-id="52a9b-103">Remove uma versão específica da API</span><span class="sxs-lookup"><span data-stu-id="52a9b-103">Removes a particular API Release</span></span>

## <span data-ttu-id="52a9b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52a9b-104">SYNTAX</span></span>

### <span data-ttu-id="52a9b-105">ByApiReleaseId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="52a9b-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52a9b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="52a9b-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52a9b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="52a9b-107">DESCRIPTION</span></span>

<span data-ttu-id="52a9b-108">O cmdlet **Remove-AzAzureRmApiManagementApiRelease** remove uma versão da API existente.</span><span class="sxs-lookup"><span data-stu-id="52a9b-108">The **Remove-AzAzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="52a9b-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="52a9b-109">EXAMPLES</span></span>

### <span data-ttu-id="52a9b-110">Exemplo 1: Remover uma versão da API</span><span class="sxs-lookup"><span data-stu-id="52a9b-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="52a9b-111">Esse comando remove o Lançamento da API com a ApiId especificada e o ReleaseId.</span><span class="sxs-lookup"><span data-stu-id="52a9b-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="52a9b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52a9b-112">PARAMETERS</span></span>

### <span data-ttu-id="52a9b-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="52a9b-113">-ApiId</span></span>
<span data-ttu-id="52a9b-114">Identificador da API.</span><span class="sxs-lookup"><span data-stu-id="52a9b-114">Identifier of the API.</span></span>
<span data-ttu-id="52a9b-115">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="52a9b-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52a9b-116">-Contexto</span><span class="sxs-lookup"><span data-stu-id="52a9b-116">-Context</span></span>
<span data-ttu-id="52a9b-117">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="52a9b-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="52a9b-118">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="52a9b-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52a9b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52a9b-119">-DefaultProfile</span></span>
<span data-ttu-id="52a9b-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52a9b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52a9b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52a9b-121">-InputObject</span></span>
<span data-ttu-id="52a9b-122">Instância de PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="52a9b-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="52a9b-123">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="52a9b-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52a9b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52a9b-124">-PassThru</span></span>
<span data-ttu-id="52a9b-125">Se especificado, a gravação será verdadeira caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="52a9b-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="52a9b-126">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="52a9b-126">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a9b-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="52a9b-127">-ReleaseId</span></span>
<span data-ttu-id="52a9b-128">Identificador do Lançamento da API.</span><span class="sxs-lookup"><span data-stu-id="52a9b-128">Identifier of the API Release.</span></span>
<span data-ttu-id="52a9b-129">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="52a9b-129">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52a9b-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="52a9b-130">-Confirm</span></span>
<span data-ttu-id="52a9b-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52a9b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52a9b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52a9b-132">-WhatIf</span></span>
<span data-ttu-id="52a9b-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="52a9b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52a9b-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52a9b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52a9b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52a9b-135">CommonParameters</span></span>
<span data-ttu-id="52a9b-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52a9b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52a9b-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52a9b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52a9b-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="52a9b-138">INPUTS</span></span>

### <span data-ttu-id="52a9b-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="52a9b-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="52a9b-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="52a9b-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

### <span data-ttu-id="52a9b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="52a9b-141">System.String</span></span>

## <span data-ttu-id="52a9b-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="52a9b-142">OUTPUTS</span></span>

### <span data-ttu-id="52a9b-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="52a9b-143">System.Boolean</span></span>

## <span data-ttu-id="52a9b-144">Notas</span><span class="sxs-lookup"><span data-stu-id="52a9b-144">NOTES</span></span>

## <span data-ttu-id="52a9b-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52a9b-145">RELATED LINKS</span></span>

[<span data-ttu-id="52a9b-146">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="52a9b-146">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="52a9b-147">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="52a9b-147">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

[<span data-ttu-id="52a9b-148">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="52a9b-148">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)