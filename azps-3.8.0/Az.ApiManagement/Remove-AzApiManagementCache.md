---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
ms.openlocfilehash: b43aba64f30c4a1987f2bcd8dec3edb7834f2082
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942228"
---
# <span data-ttu-id="8c872-101">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="8c872-101">Remove-AzApiManagementCache</span></span>

## <span data-ttu-id="8c872-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c872-102">SYNOPSIS</span></span>
<span data-ttu-id="8c872-103">Remove a entidade de cache.</span><span class="sxs-lookup"><span data-stu-id="8c872-103">Removes the cache entity.</span></span>

## <span data-ttu-id="8c872-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c872-104">SYNTAX</span></span>

### <span data-ttu-id="8c872-105">ContextParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="8c872-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c872-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c872-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementCache -InputObject <PsApiManagementCache> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c872-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c872-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementCache -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c872-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c872-108">DESCRIPTION</span></span>
<span data-ttu-id="8c872-109">O cmdlet **Remove-AzApiManagementCache** remove a entidade cache.</span><span class="sxs-lookup"><span data-stu-id="8c872-109">The cmdlet **Remove-AzApiManagementCache** removes the cache entity.</span></span>

## <span data-ttu-id="8c872-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c872-110">EXAMPLES</span></span>

### <span data-ttu-id="8c872-111">Exemplo 1: remover a entidade de cache</span><span class="sxs-lookup"><span data-stu-id="8c872-111">Example 1 : Remove the Cache entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCache -Context $apimContext -CacheId "centralus"
```

<span data-ttu-id="8c872-112">Este cmdlet Remove o cache `centralus` do serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="8c872-112">This cmdlet remove the cache `centralus` from Api Management service.</span></span>

## <span data-ttu-id="8c872-113">OS</span><span class="sxs-lookup"><span data-stu-id="8c872-113">PARAMETERS</span></span>

### <span data-ttu-id="8c872-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="8c872-114">-CacheId</span></span>
<span data-ttu-id="8c872-115">Identificador de CacheId existente.</span><span class="sxs-lookup"><span data-stu-id="8c872-115">Identifier of existing cacheId.</span></span>
<span data-ttu-id="8c872-116">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="8c872-116">This parameter is required.</span></span>

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

### <span data-ttu-id="8c872-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="8c872-117">-Context</span></span>
<span data-ttu-id="8c872-118">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8c872-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8c872-119">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="8c872-119">This parameter is required.</span></span>

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

### <span data-ttu-id="8c872-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c872-120">-DefaultProfile</span></span>
<span data-ttu-id="8c872-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8c872-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c872-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c872-122">-InputObject</span></span>
<span data-ttu-id="8c872-123">Instância do PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="8c872-123">Instance of PsApiManagementCache.</span></span> <span data-ttu-id="8c872-124">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="8c872-124">This parameter is required.</span></span>

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

### <span data-ttu-id="8c872-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c872-125">-PassThru</span></span>
<span data-ttu-id="8c872-126">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8c872-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="8c872-127">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="8c872-127">This parameter is optional.</span></span>
<span data-ttu-id="8c872-128">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="8c872-128">Default value is false.</span></span>

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

### <span data-ttu-id="8c872-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c872-129">-ResourceId</span></span>
<span data-ttu-id="8c872-130">Resourcebinding do cache.</span><span class="sxs-lookup"><span data-stu-id="8c872-130">Arm ResourceId of Cache.</span></span> <span data-ttu-id="8c872-131">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="8c872-131">This parameter is required.</span></span>

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

### <span data-ttu-id="8c872-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8c872-132">-Confirm</span></span>
<span data-ttu-id="8c872-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c872-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c872-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c872-134">-WhatIf</span></span>
<span data-ttu-id="8c872-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8c872-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c872-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8c872-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c872-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c872-137">CommonParameters</span></span>
<span data-ttu-id="8c872-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c872-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c872-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c872-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c872-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c872-140">INPUTS</span></span>

### <span data-ttu-id="8c872-141">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8c872-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8c872-142">System. String</span><span class="sxs-lookup"><span data-stu-id="8c872-142">System.String</span></span>

### <span data-ttu-id="8c872-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8c872-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8c872-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c872-144">OUTPUTS</span></span>

### <span data-ttu-id="8c872-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8c872-145">System.Boolean</span></span>

## <span data-ttu-id="8c872-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c872-146">NOTES</span></span>

## <span data-ttu-id="8c872-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c872-147">RELATED LINKS</span></span>

[<span data-ttu-id="8c872-148">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="8c872-148">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache)

[<span data-ttu-id="8c872-149">Set-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="8c872-149">Set-AzApiManagementCache</span></span>](./Set-AzApiManagementCache.md)

[<span data-ttu-id="8c872-150">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="8c872-150">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)