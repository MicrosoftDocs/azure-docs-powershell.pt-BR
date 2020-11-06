---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/publish-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: b9963fc53a146a2e8c76ac9b15166f0de6ba67ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598013"
---
# <span data-ttu-id="ca8c1-101">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca8c1-101">Publish-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="ca8c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca8c1-102">SYNOPSIS</span></span>
<span data-ttu-id="ca8c1-103">Publica alterações de uma ramificação git para o banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="ca8c1-103">Publishes changes from a Git branch to the configuration database.</span></span>

## <span data-ttu-id="ca8c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca8c1-104">SYNTAX</span></span>

```
Publish-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca8c1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca8c1-105">DESCRIPTION</span></span>
<span data-ttu-id="ca8c1-106">O cmdlet **Publish-AzApiManagementTenantGitConfiguration** publica as alterações de uma ramificação git para o banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="ca8c1-106">The **Publish-AzApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="ca8c1-107">Você também pode validar as alterações em uma ramificação git sem publicar.</span><span class="sxs-lookup"><span data-stu-id="ca8c1-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="ca8c1-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca8c1-108">EXAMPLES</span></span>

### <span data-ttu-id="ca8c1-109">Exemplo 1: implantar alterações no git</span><span class="sxs-lookup"><span data-stu-id="ca8c1-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="ca8c1-110">Esse comando publica as alterações da ramificação especificada para o banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="ca8c1-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="ca8c1-111">Exemplo 2: validar alterações do git</span><span class="sxs-lookup"><span data-stu-id="ca8c1-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="ca8c1-112">Esse comando valida as alterações na ramificação git em relação ao banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="ca8c1-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="ca8c1-113">Ele não publica alterações.</span><span class="sxs-lookup"><span data-stu-id="ca8c1-113">It does not publish changes.</span></span>

## <span data-ttu-id="ca8c1-114">OS</span><span class="sxs-lookup"><span data-stu-id="ca8c1-114">PARAMETERS</span></span>

### <span data-ttu-id="ca8c1-115">-Ramificação</span><span class="sxs-lookup"><span data-stu-id="ca8c1-115">-Branch</span></span>
<span data-ttu-id="ca8c1-116">Especifica o nome da ramificação git da qual esse cmdlet implanta a configuração para o banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="ca8c1-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="ca8c1-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="ca8c1-117">-Context</span></span>
<span data-ttu-id="ca8c1-118">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ca8c1-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ca8c1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca8c1-119">-DefaultProfile</span></span>
<span data-ttu-id="ca8c1-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca8c1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca8c1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ca8c1-121">-Force</span></span>
<span data-ttu-id="ca8c1-122">Indica que esse cmdlet exclui assinaturas para produtos que são excluídos nesta atualização.</span><span class="sxs-lookup"><span data-stu-id="ca8c1-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

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

### <span data-ttu-id="ca8c1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca8c1-123">-PassThru</span></span>
<span data-ttu-id="ca8c1-124">Indica que esse cmdlet retorna um objeto **PsApiManagementOperationResult** .</span><span class="sxs-lookup"><span data-stu-id="ca8c1-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="ca8c1-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="ca8c1-125">-ValidateOnly</span></span>
<span data-ttu-id="ca8c1-126">Indica que esse cmdlet valida as alterações na ramificação git especificada.</span><span class="sxs-lookup"><span data-stu-id="ca8c1-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="ca8c1-127">Ele não publica no banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="ca8c1-127">It does not publish to the configuration database.</span></span>

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

### <span data-ttu-id="ca8c1-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ca8c1-128">-Confirm</span></span>
<span data-ttu-id="ca8c1-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca8c1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca8c1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca8c1-130">-WhatIf</span></span>
<span data-ttu-id="ca8c1-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ca8c1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca8c1-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca8c1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca8c1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca8c1-133">CommonParameters</span></span>
<span data-ttu-id="ca8c1-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca8c1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca8c1-135">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca8c1-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca8c1-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca8c1-136">INPUTS</span></span>

### <span data-ttu-id="ca8c1-137">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ca8c1-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ca8c1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ca8c1-138">System.String</span></span>

### <span data-ttu-id="ca8c1-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ca8c1-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ca8c1-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca8c1-140">OUTPUTS</span></span>

### <span data-ttu-id="ca8c1-141">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="ca8c1-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="ca8c1-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca8c1-142">NOTES</span></span>

## <span data-ttu-id="ca8c1-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca8c1-143">RELATED LINKS</span></span>

[<span data-ttu-id="ca8c1-144">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca8c1-144">Save-AzApiManagementTenantGitConfiguration</span></span>](./Save-AzApiManagementTenantGitConfiguration.md)


