---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/publish-azurermapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 24c5bb33982d7bc4fb5209133022358a2dee5486
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431464"
---
# <span data-ttu-id="cc186-101">Publish-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc186-101">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="cc186-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc186-102">SYNOPSIS</span></span>
<span data-ttu-id="cc186-103">Publica alterações de uma ramificação git para o banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="cc186-103">Publishes changes from a Git branch to the configuration database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc186-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc186-104">SYNTAX</span></span>

```
Publish-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cc186-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cc186-105">DESCRIPTION</span></span>
<span data-ttu-id="cc186-106">O cmdlet **Publish-AzureRmApiManagementTenantGitConfiguration** publica as alterações de uma ramificação git para o banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="cc186-106">The **Publish-AzureRmApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="cc186-107">Você também pode validar as alterações em uma ramificação git sem publicar.</span><span class="sxs-lookup"><span data-stu-id="cc186-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="cc186-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc186-108">EXAMPLES</span></span>

### <span data-ttu-id="cc186-109">Exemplo 1: implantar alterações no git</span><span class="sxs-lookup"><span data-stu-id="cc186-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="cc186-110">Esse comando publica as alterações da ramificação especificada para o banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="cc186-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="cc186-111">Exemplo 2: validar alterações do git</span><span class="sxs-lookup"><span data-stu-id="cc186-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="cc186-112">Esse comando valida as alterações na ramificação git em relação ao banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="cc186-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="cc186-113">Ele não publica alterações.</span><span class="sxs-lookup"><span data-stu-id="cc186-113">It does not publish changes.</span></span>

## <span data-ttu-id="cc186-114">OS</span><span class="sxs-lookup"><span data-stu-id="cc186-114">PARAMETERS</span></span>

### <span data-ttu-id="cc186-115">-Ramificação</span><span class="sxs-lookup"><span data-stu-id="cc186-115">-Branch</span></span>
<span data-ttu-id="cc186-116">Especifica o nome da ramificação git da qual esse cmdlet implanta a configuração para o banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="cc186-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="cc186-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="cc186-117">-Context</span></span>
<span data-ttu-id="cc186-118">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="cc186-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="cc186-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc186-119">-DefaultProfile</span></span>
<span data-ttu-id="cc186-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc186-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc186-121">-Force</span><span class="sxs-lookup"><span data-stu-id="cc186-121">-Force</span></span>
<span data-ttu-id="cc186-122">Indica que esse cmdlet exclui assinaturas para produtos que são excluídos nesta atualização.</span><span class="sxs-lookup"><span data-stu-id="cc186-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

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

### <span data-ttu-id="cc186-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc186-123">-PassThru</span></span>
<span data-ttu-id="cc186-124">Indica que esse cmdlet retorna um objeto **PsApiManagementOperationResult** .</span><span class="sxs-lookup"><span data-stu-id="cc186-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="cc186-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="cc186-125">-ValidateOnly</span></span>
<span data-ttu-id="cc186-126">Indica que esse cmdlet valida as alterações na ramificação git especificada.</span><span class="sxs-lookup"><span data-stu-id="cc186-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="cc186-127">Ele não publica no banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="cc186-127">It does not publish to the configuration database.</span></span>

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

### <span data-ttu-id="cc186-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cc186-128">-Confirm</span></span>
<span data-ttu-id="cc186-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc186-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc186-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc186-130">-WhatIf</span></span>
<span data-ttu-id="cc186-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cc186-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc186-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cc186-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc186-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc186-133">CommonParameters</span></span>
<span data-ttu-id="cc186-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc186-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc186-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc186-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc186-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cc186-136">INPUTS</span></span>

### <span data-ttu-id="cc186-137">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cc186-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cc186-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cc186-138">System.String</span></span>

### <span data-ttu-id="cc186-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cc186-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cc186-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cc186-140">OUTPUTS</span></span>

### <span data-ttu-id="cc186-141">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="cc186-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="cc186-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cc186-142">NOTES</span></span>

## <span data-ttu-id="cc186-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc186-143">RELATED LINKS</span></span>

[<span data-ttu-id="cc186-144">Save-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc186-144">Save-AzureRmApiManagementTenantGitConfiguration</span></span>](./Save-AzureRmApiManagementTenantGitConfiguration.md)


