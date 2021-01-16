---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
ms.openlocfilehash: ffca6c1bc32d809f7bbb93c3b76dd9490f9fafb8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262923"
---
# <span data-ttu-id="b485d-101">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b485d-101">Remove-AzApiManagementCache</span></span>

## <span data-ttu-id="b485d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b485d-102">SYNOPSIS</span></span>
<span data-ttu-id="b485d-103">Remove a entidade de cache.</span><span class="sxs-lookup"><span data-stu-id="b485d-103">Removes the cache entity.</span></span>

## <span data-ttu-id="b485d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b485d-104">SYNTAX</span></span>

### <span data-ttu-id="b485d-105">ContextParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="b485d-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b485d-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b485d-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementCache -InputObject <PsApiManagementCache> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b485d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b485d-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementCache -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b485d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b485d-108">DESCRIPTION</span></span>
<span data-ttu-id="b485d-109">O cmdlet **Remove-AzApiManagementCache** remove a entidade cache.</span><span class="sxs-lookup"><span data-stu-id="b485d-109">The cmdlet **Remove-AzApiManagementCache** removes the cache entity.</span></span>

## <span data-ttu-id="b485d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b485d-110">EXAMPLES</span></span>

### <span data-ttu-id="b485d-111">Exemplo 1: remover a entidade de cache</span><span class="sxs-lookup"><span data-stu-id="b485d-111">Example 1 : Remove the Cache entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCache -Context $apimContext -CacheId "centralus"
```

<span data-ttu-id="b485d-112">Este cmdlet Remove o cache `centralus` do serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="b485d-112">This cmdlet remove the cache `centralus` from Api Management service.</span></span>

## <span data-ttu-id="b485d-113">OS</span><span class="sxs-lookup"><span data-stu-id="b485d-113">PARAMETERS</span></span>

### <span data-ttu-id="b485d-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="b485d-114">-CacheId</span></span>
<span data-ttu-id="b485d-115">Identificador de CacheId existente.</span><span class="sxs-lookup"><span data-stu-id="b485d-115">Identifier of existing cacheId.</span></span>
<span data-ttu-id="b485d-116">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="b485d-116">This parameter is required.</span></span>

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

### <span data-ttu-id="b485d-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="b485d-117">-Context</span></span>
<span data-ttu-id="b485d-118">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b485d-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b485d-119">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="b485d-119">This parameter is required.</span></span>

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

### <span data-ttu-id="b485d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b485d-120">-DefaultProfile</span></span>
<span data-ttu-id="b485d-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b485d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b485d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b485d-122">-InputObject</span></span>
<span data-ttu-id="b485d-123">Instância do PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="b485d-123">Instance of PsApiManagementCache.</span></span> <span data-ttu-id="b485d-124">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="b485d-124">This parameter is required.</span></span>

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

### <span data-ttu-id="b485d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b485d-125">-PassThru</span></span>
<span data-ttu-id="b485d-126">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b485d-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="b485d-127">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b485d-127">This parameter is optional.</span></span>
<span data-ttu-id="b485d-128">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="b485d-128">Default value is false.</span></span>

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

### <span data-ttu-id="b485d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b485d-129">-ResourceId</span></span>
<span data-ttu-id="b485d-130">Resourcebinding do cache.</span><span class="sxs-lookup"><span data-stu-id="b485d-130">Arm ResourceId of Cache.</span></span> <span data-ttu-id="b485d-131">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="b485d-131">This parameter is required.</span></span>

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

### <span data-ttu-id="b485d-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b485d-132">-Confirm</span></span>
<span data-ttu-id="b485d-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b485d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b485d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b485d-134">-WhatIf</span></span>
<span data-ttu-id="b485d-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b485d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b485d-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b485d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b485d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b485d-137">CommonParameters</span></span>
<span data-ttu-id="b485d-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b485d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b485d-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b485d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b485d-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b485d-140">INPUTS</span></span>

### <span data-ttu-id="b485d-141">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b485d-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b485d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b485d-142">System.String</span></span>

### <span data-ttu-id="b485d-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b485d-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b485d-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b485d-144">OUTPUTS</span></span>

### <span data-ttu-id="b485d-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b485d-145">System.Boolean</span></span>

## <span data-ttu-id="b485d-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b485d-146">NOTES</span></span>

## <span data-ttu-id="b485d-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b485d-147">RELATED LINKS</span></span>

[<span data-ttu-id="b485d-148">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b485d-148">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="b485d-149">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b485d-149">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="b485d-150">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b485d-150">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
