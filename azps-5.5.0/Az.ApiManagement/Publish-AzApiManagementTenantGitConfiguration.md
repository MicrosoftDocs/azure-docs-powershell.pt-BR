---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/publish-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 288bb02ffad3669615df3535aec7f691162daa2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112308"
---
# <span data-ttu-id="0a164-101">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a164-101">Publish-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="0a164-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a164-102">SYNOPSIS</span></span>
<span data-ttu-id="0a164-103">Publica alterações de uma ramificação git no banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="0a164-103">Publishes changes from a Git branch to the configuration database.</span></span>

## <span data-ttu-id="0a164-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a164-104">SYNTAX</span></span>

```
Publish-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a164-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a164-105">DESCRIPTION</span></span>
<span data-ttu-id="0a164-106">O cmdlet **Publish-AzApiManagementTenantGitConfiguration** publica as alterações de uma ramificação git para o banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="0a164-106">The **Publish-AzApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="0a164-107">Você pode validar as alterações em uma ramificação git sem publicar.</span><span class="sxs-lookup"><span data-stu-id="0a164-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="0a164-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0a164-108">EXAMPLES</span></span>

### <span data-ttu-id="0a164-109">Exemplo 1: Implantar alterações no Git</span><span class="sxs-lookup"><span data-stu-id="0a164-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="0a164-110">Esse comando publica as alterações da ramificação especificada no banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="0a164-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="0a164-111">Exemplo 2: Validar alterações do Git</span><span class="sxs-lookup"><span data-stu-id="0a164-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="0a164-112">Esse comando valida as alterações na ramificação git em relação ao banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="0a164-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="0a164-113">Ele não publica alterações.</span><span class="sxs-lookup"><span data-stu-id="0a164-113">It does not publish changes.</span></span>

## <span data-ttu-id="0a164-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a164-114">PARAMETERS</span></span>

### <span data-ttu-id="0a164-115">-Branch</span><span class="sxs-lookup"><span data-stu-id="0a164-115">-Branch</span></span>
<span data-ttu-id="0a164-116">Especifica o nome da ramificação Git a partir da qual este cmdlet implanta a configuração para o banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="0a164-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="0a164-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="0a164-117">-Context</span></span>
<span data-ttu-id="0a164-118">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="0a164-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a164-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a164-119">-DefaultProfile</span></span>
<span data-ttu-id="0a164-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0a164-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a164-121">-Forçar</span><span class="sxs-lookup"><span data-stu-id="0a164-121">-Force</span></span>
<span data-ttu-id="0a164-122">Indica que esse cmdlet exclui assinaturas de produtos excluídos nesta atualização.</span><span class="sxs-lookup"><span data-stu-id="0a164-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

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

### <span data-ttu-id="0a164-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a164-123">-PassThru</span></span>
<span data-ttu-id="0a164-124">Indica que esse cmdlet retorna um **objeto PsApiManagementOperationResult.**</span><span class="sxs-lookup"><span data-stu-id="0a164-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="0a164-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="0a164-125">-ValidateOnly</span></span>
<span data-ttu-id="0a164-126">Indica que esse cmdlet valida as alterações na ramificação do Git especificada.</span><span class="sxs-lookup"><span data-stu-id="0a164-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="0a164-127">Ele não é publicado no banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="0a164-127">It does not publish to the configuration database.</span></span>

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

### <span data-ttu-id="0a164-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0a164-128">-Confirm</span></span>
<span data-ttu-id="0a164-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a164-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a164-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a164-130">-WhatIf</span></span>
<span data-ttu-id="0a164-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0a164-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a164-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0a164-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a164-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a164-133">CommonParameters</span></span>
<span data-ttu-id="0a164-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a164-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a164-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a164-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a164-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="0a164-136">INPUTS</span></span>

### <span data-ttu-id="0a164-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0a164-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0a164-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0a164-138">System.String</span></span>

### <span data-ttu-id="0a164-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0a164-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0a164-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="0a164-140">OUTPUTS</span></span>

### <span data-ttu-id="0a164-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="0a164-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="0a164-142">Notas</span><span class="sxs-lookup"><span data-stu-id="0a164-142">NOTES</span></span>

## <span data-ttu-id="0a164-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a164-143">RELATED LINKS</span></span>

[<span data-ttu-id="0a164-144">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a164-144">Save-AzApiManagementTenantGitConfiguration</span></span>](./Save-AzApiManagementTenantGitConfiguration.md)


