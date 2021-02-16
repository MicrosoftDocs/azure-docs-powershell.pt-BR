---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
ms.openlocfilehash: a95be9f18c00d72afb6117d1689f62a6bad053b4
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398675"
---
# <span data-ttu-id="3b7a3-101">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="3b7a3-101">Remove-AzApiManagementCache</span></span>

## <span data-ttu-id="3b7a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b7a3-102">SYNOPSIS</span></span>
<span data-ttu-id="3b7a3-103">Remove a entidade de cache.</span><span class="sxs-lookup"><span data-stu-id="3b7a3-103">Removes the cache entity.</span></span>

## <span data-ttu-id="3b7a3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b7a3-104">SYNTAX</span></span>

### <span data-ttu-id="3b7a3-105">ContextParameterSetName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3b7a3-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b7a3-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b7a3-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementCache -InputObject <PsApiManagementCache> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b7a3-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b7a3-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementCache -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b7a3-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b7a3-108">DESCRIPTION</span></span>
<span data-ttu-id="3b7a3-109">O cmdlet **Remove-AzApiManagementCache** remove a entidade de cache.</span><span class="sxs-lookup"><span data-stu-id="3b7a3-109">The cmdlet **Remove-AzApiManagementCache** removes the cache entity.</span></span>

## <span data-ttu-id="3b7a3-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3b7a3-110">EXAMPLES</span></span>

### <span data-ttu-id="3b7a3-111">Exemplo 1: Remover a entidade Cache</span><span class="sxs-lookup"><span data-stu-id="3b7a3-111">Example 1 : Remove the Cache entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCache -Context $apimContext -CacheId "centralus"
```

<span data-ttu-id="3b7a3-112">Este cmdlet remove o cache `centralus` do serviço de Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="3b7a3-112">This cmdlet remove the cache `centralus` from Api Management service.</span></span>

## <span data-ttu-id="3b7a3-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b7a3-113">PARAMETERS</span></span>

### <span data-ttu-id="3b7a3-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="3b7a3-114">-CacheId</span></span>
<span data-ttu-id="3b7a3-115">Identificador de cacheId existente.</span><span class="sxs-lookup"><span data-stu-id="3b7a3-115">Identifier of existing cacheId.</span></span>
<span data-ttu-id="3b7a3-116">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="3b7a3-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b7a3-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="3b7a3-117">-Context</span></span>
<span data-ttu-id="3b7a3-118">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3b7a3-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3b7a3-119">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="3b7a3-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b7a3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b7a3-120">-DefaultProfile</span></span>
<span data-ttu-id="3b7a3-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3b7a3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b7a3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b7a3-122">-InputObject</span></span>
<span data-ttu-id="3b7a3-123">Instância de PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="3b7a3-123">Instance of PsApiManagementCache.</span></span> <span data-ttu-id="3b7a3-124">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="3b7a3-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b7a3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b7a3-125">-PassThru</span></span>
<span data-ttu-id="3b7a3-126">Se especificado, a gravação será verdadeira caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3b7a3-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="3b7a3-127">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="3b7a3-127">This parameter is optional.</span></span>
<span data-ttu-id="3b7a3-128">O valor padrão é falso.</span><span class="sxs-lookup"><span data-stu-id="3b7a3-128">Default value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b7a3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b7a3-129">-ResourceId</span></span>
<span data-ttu-id="3b7a3-130">Arm ResourceId of Cache.</span><span class="sxs-lookup"><span data-stu-id="3b7a3-130">Arm ResourceId of Cache.</span></span> <span data-ttu-id="3b7a3-131">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="3b7a3-131">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b7a3-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3b7a3-132">-Confirm</span></span>
<span data-ttu-id="3b7a3-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b7a3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b7a3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b7a3-134">-WhatIf</span></span>
<span data-ttu-id="3b7a3-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3b7a3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b7a3-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3b7a3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b7a3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b7a3-137">CommonParameters</span></span>
<span data-ttu-id="3b7a3-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b7a3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b7a3-139">Para obter mais informações, [consulte about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b7a3-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b7a3-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="3b7a3-140">INPUTS</span></span>

### <span data-ttu-id="3b7a3-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3b7a3-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3b7a3-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3b7a3-142">System.String</span></span>

### <span data-ttu-id="3b7a3-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3b7a3-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3b7a3-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="3b7a3-144">OUTPUTS</span></span>

### <span data-ttu-id="3b7a3-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3b7a3-145">System.Boolean</span></span>

## <span data-ttu-id="3b7a3-146">Notas</span><span class="sxs-lookup"><span data-stu-id="3b7a3-146">NOTES</span></span>

## <span data-ttu-id="3b7a3-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b7a3-147">RELATED LINKS</span></span>

[<span data-ttu-id="3b7a3-148">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="3b7a3-148">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="3b7a3-149">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="3b7a3-149">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="3b7a3-150">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="3b7a3-150">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
