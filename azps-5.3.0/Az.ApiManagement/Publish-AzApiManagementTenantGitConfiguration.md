---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/publish-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 288bb02ffad3669615df3535aec7f691162daa2a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272192"
---
# <span data-ttu-id="a18a4-101">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="a18a4-101">Publish-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="a18a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a18a4-102">SYNOPSIS</span></span>
<span data-ttu-id="a18a4-103">Publica alterações de uma ramificação git para o banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="a18a4-103">Publishes changes from a Git branch to the configuration database.</span></span>

## <span data-ttu-id="a18a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a18a4-104">SYNTAX</span></span>

```
Publish-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a18a4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a18a4-105">DESCRIPTION</span></span>
<span data-ttu-id="a18a4-106">O cmdlet **Publish-AzApiManagementTenantGitConfiguration** publica as alterações de uma ramificação git para o banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="a18a4-106">The **Publish-AzApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="a18a4-107">Você também pode validar as alterações em uma ramificação git sem publicar.</span><span class="sxs-lookup"><span data-stu-id="a18a4-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="a18a4-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a18a4-108">EXAMPLES</span></span>

### <span data-ttu-id="a18a4-109">Exemplo 1: implantar alterações no git</span><span class="sxs-lookup"><span data-stu-id="a18a4-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="a18a4-110">Esse comando publica as alterações da ramificação especificada para o banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="a18a4-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="a18a4-111">Exemplo 2: validar alterações do git</span><span class="sxs-lookup"><span data-stu-id="a18a4-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="a18a4-112">Esse comando valida as alterações na ramificação git em relação ao banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="a18a4-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="a18a4-113">Ele não publica alterações.</span><span class="sxs-lookup"><span data-stu-id="a18a4-113">It does not publish changes.</span></span>

## <span data-ttu-id="a18a4-114">OS</span><span class="sxs-lookup"><span data-stu-id="a18a4-114">PARAMETERS</span></span>

### <span data-ttu-id="a18a4-115">-Ramificação</span><span class="sxs-lookup"><span data-stu-id="a18a4-115">-Branch</span></span>
<span data-ttu-id="a18a4-116">Especifica o nome da ramificação git da qual esse cmdlet implanta a configuração para o banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="a18a4-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="a18a4-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="a18a4-117">-Context</span></span>
<span data-ttu-id="a18a4-118">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a18a4-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a18a4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a18a4-119">-DefaultProfile</span></span>
<span data-ttu-id="a18a4-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a18a4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a18a4-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a18a4-121">-Force</span></span>
<span data-ttu-id="a18a4-122">Indica que esse cmdlet exclui assinaturas para produtos que são excluídos nesta atualização.</span><span class="sxs-lookup"><span data-stu-id="a18a4-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

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

### <span data-ttu-id="a18a4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a18a4-123">-PassThru</span></span>
<span data-ttu-id="a18a4-124">Indica que esse cmdlet retorna um objeto **PsApiManagementOperationResult** .</span><span class="sxs-lookup"><span data-stu-id="a18a4-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="a18a4-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="a18a4-125">-ValidateOnly</span></span>
<span data-ttu-id="a18a4-126">Indica que esse cmdlet valida as alterações na ramificação git especificada.</span><span class="sxs-lookup"><span data-stu-id="a18a4-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="a18a4-127">Ele não publica no banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="a18a4-127">It does not publish to the configuration database.</span></span>

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

### <span data-ttu-id="a18a4-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a18a4-128">-Confirm</span></span>
<span data-ttu-id="a18a4-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a18a4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a18a4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a18a4-130">-WhatIf</span></span>
<span data-ttu-id="a18a4-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a18a4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a18a4-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a18a4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a18a4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a18a4-133">CommonParameters</span></span>
<span data-ttu-id="a18a4-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a18a4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a18a4-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a18a4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a18a4-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a18a4-136">INPUTS</span></span>

### <span data-ttu-id="a18a4-137">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a18a4-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a18a4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a18a4-138">System.String</span></span>

### <span data-ttu-id="a18a4-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a18a4-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a18a4-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a18a4-140">OUTPUTS</span></span>

### <span data-ttu-id="a18a4-141">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="a18a4-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="a18a4-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a18a4-142">NOTES</span></span>

## <span data-ttu-id="a18a4-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a18a4-143">RELATED LINKS</span></span>

[<span data-ttu-id="a18a4-144">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="a18a4-144">Save-AzApiManagementTenantGitConfiguration</span></span>](./Save-AzApiManagementTenantGitConfiguration.md)


