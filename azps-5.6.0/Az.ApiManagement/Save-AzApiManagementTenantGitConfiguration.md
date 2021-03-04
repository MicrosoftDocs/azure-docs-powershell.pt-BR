---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/save-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: eb865535fcb4ee49b834e923fcf3f319ff5de074
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887076"
---
# <span data-ttu-id="14ca5-101">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="14ca5-101">Save-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="14ca5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14ca5-102">SYNOPSIS</span></span>
<span data-ttu-id="14ca5-103">Salva as alterações criando uma confirmação para a configuração atual.</span><span class="sxs-lookup"><span data-stu-id="14ca5-103">Saves changes by creating a commit for current configuration.</span></span>

## <span data-ttu-id="14ca5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="14ca5-104">SYNTAX</span></span>

```
Save-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14ca5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="14ca5-105">DESCRIPTION</span></span>
<span data-ttu-id="14ca5-106">O cmdlet **Save-AzApiManagementTenantGitConfiguration** salva as alterações criando uma confirmação que contém o instantâneo de configuração atual em um branch no repositório.</span><span class="sxs-lookup"><span data-stu-id="14ca5-106">The **Save-AzApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="14ca5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14ca5-107">EXAMPLES</span></span>

### <span data-ttu-id="14ca5-108">Exemplo 1: Salvar alterações na configuração</span><span class="sxs-lookup"><span data-stu-id="14ca5-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="14ca5-109">Esse comando salva as alterações criando uma confirmação com o instantâneo de configuração atual para o branch especificado no repositório.</span><span class="sxs-lookup"><span data-stu-id="14ca5-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="14ca5-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="14ca5-110">PARAMETERS</span></span>

### <span data-ttu-id="14ca5-111">-Branch</span><span class="sxs-lookup"><span data-stu-id="14ca5-111">-Branch</span></span>
<span data-ttu-id="14ca5-112">Especifica o nome da ramificação Git na qual o instantâneo de configuração atual será confirmado.</span><span class="sxs-lookup"><span data-stu-id="14ca5-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="14ca5-113">-Context</span><span class="sxs-lookup"><span data-stu-id="14ca5-113">-Context</span></span>
<span data-ttu-id="14ca5-114">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="14ca5-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14ca5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14ca5-115">-DefaultProfile</span></span>
<span data-ttu-id="14ca5-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="14ca5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14ca5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="14ca5-117">-Force</span></span>
<span data-ttu-id="14ca5-118">Especifica que esse cmdlet confirma o banco de dados de configuração atual para o repositório git, mesmo que o repositório git tenha alterações mais novas que são substituídas.</span><span class="sxs-lookup"><span data-stu-id="14ca5-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="14ca5-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14ca5-119">-PassThru</span></span>
<span data-ttu-id="14ca5-120">Indica que esse cmdlet retorna um **objeto PsApiManagementOperationResult.**</span><span class="sxs-lookup"><span data-stu-id="14ca5-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="14ca5-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14ca5-121">-Confirm</span></span>
<span data-ttu-id="14ca5-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14ca5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14ca5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14ca5-123">-WhatIf</span></span>
<span data-ttu-id="14ca5-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14ca5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14ca5-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14ca5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14ca5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14ca5-126">CommonParameters</span></span>
<span data-ttu-id="14ca5-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14ca5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14ca5-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14ca5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14ca5-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14ca5-129">INPUTS</span></span>

### <span data-ttu-id="14ca5-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="14ca5-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="14ca5-131">System.String</span><span class="sxs-lookup"><span data-stu-id="14ca5-131">System.String</span></span>

### <span data-ttu-id="14ca5-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="14ca5-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="14ca5-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="14ca5-133">OUTPUTS</span></span>

### <span data-ttu-id="14ca5-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="14ca5-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="14ca5-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="14ca5-135">NOTES</span></span>

## <span data-ttu-id="14ca5-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14ca5-136">RELATED LINKS</span></span>

[<span data-ttu-id="14ca5-137">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="14ca5-137">Publish-AzApiManagementTenantGitConfiguration</span></span>](./Publish-AzApiManagementTenantGitConfiguration.md)


