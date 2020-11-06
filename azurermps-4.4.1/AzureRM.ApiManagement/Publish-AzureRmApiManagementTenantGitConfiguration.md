---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 2a867109bf44cd652eaf1d256d963796e06762cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428016"
---
# <span data-ttu-id="7075f-101">Publish-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="7075f-101">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="7075f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7075f-102">SYNOPSIS</span></span>
<span data-ttu-id="7075f-103">Publica alterações de uma ramificação git para o banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="7075f-103">Publishes changes from a Git branch to the configuration database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7075f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7075f-104">SYNTAX</span></span>

```
Publish-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7075f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7075f-105">DESCRIPTION</span></span>
<span data-ttu-id="7075f-106">O cmdlet **Publish-AzureRmApiManagementTenantGitConfiguration** publica as alterações de uma ramificação git para o banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="7075f-106">The **Publish-AzureRmApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="7075f-107">Você também pode validar as alterações em uma ramificação git sem publicar.</span><span class="sxs-lookup"><span data-stu-id="7075f-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="7075f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7075f-108">EXAMPLES</span></span>

### <span data-ttu-id="7075f-109">Exemplo 1: implantar alterações no git</span><span class="sxs-lookup"><span data-stu-id="7075f-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $ApimContext -Branch 'master' -PassThru
```

<span data-ttu-id="7075f-110">Esse comando publica as alterações da ramificação especificada para o banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="7075f-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="7075f-111">Exemplo 2: validar alterações do git</span><span class="sxs-lookup"><span data-stu-id="7075f-111">Example 2: Validate Git changes</span></span>
```
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $ApimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="7075f-112">Esse comando valida as alterações na ramificação git em relação ao banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="7075f-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="7075f-113">Ele não publica alterações.</span><span class="sxs-lookup"><span data-stu-id="7075f-113">It does not publish changes.</span></span>

## <span data-ttu-id="7075f-114">OS</span><span class="sxs-lookup"><span data-stu-id="7075f-114">PARAMETERS</span></span>

### <span data-ttu-id="7075f-115">-Ramificação</span><span class="sxs-lookup"><span data-stu-id="7075f-115">-Branch</span></span>
<span data-ttu-id="7075f-116">Especifica o nome da ramificação git da qual esse cmdlet implanta a configuração para o banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="7075f-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="7075f-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="7075f-117">-Context</span></span>
<span data-ttu-id="7075f-118">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="7075f-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7075f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7075f-119">-Force</span></span>
<span data-ttu-id="7075f-120">Indica que esse cmdlet exclui assinaturas para produtos que são excluídos nesta atualização.</span><span class="sxs-lookup"><span data-stu-id="7075f-120">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

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

### <span data-ttu-id="7075f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7075f-121">-PassThru</span></span>
<span data-ttu-id="7075f-122">Indica que esse cmdlet retorna um objeto **PsApiManagementOperationResult** .</span><span class="sxs-lookup"><span data-stu-id="7075f-122">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="7075f-123">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="7075f-123">-ValidateOnly</span></span>
<span data-ttu-id="7075f-124">Indica que esse cmdlet valida as alterações na ramificação git especificada.</span><span class="sxs-lookup"><span data-stu-id="7075f-124">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="7075f-125">Ele não publica no banco de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="7075f-125">It does not publish to the configuration database.</span></span>

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

### <span data-ttu-id="7075f-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7075f-126">-Confirm</span></span>
<span data-ttu-id="7075f-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7075f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7075f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7075f-128">-WhatIf</span></span>
<span data-ttu-id="7075f-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7075f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7075f-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7075f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7075f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7075f-131">-DefaultProfile</span></span>
<span data-ttu-id="7075f-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7075f-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7075f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7075f-133">CommonParameters</span></span>
<span data-ttu-id="7075f-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7075f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7075f-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7075f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7075f-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7075f-136">INPUTS</span></span>

## <span data-ttu-id="7075f-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7075f-137">OUTPUTS</span></span>

### <span data-ttu-id="7075f-138">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="7075f-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="7075f-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7075f-139">NOTES</span></span>

## <span data-ttu-id="7075f-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7075f-140">RELATED LINKS</span></span>

[<span data-ttu-id="7075f-141">Save-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="7075f-141">Save-AzureRmApiManagementTenantGitConfiguration</span></span>](./Save-AzureRmApiManagementTenantGitConfiguration.md)


