---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/save-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: b4abd2d8dab9e4c41d2e42be77bee62428ccc712
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771355"
---
# <span data-ttu-id="c0c47-101">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0c47-101">Save-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="c0c47-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c0c47-102">SYNOPSIS</span></span>
<span data-ttu-id="c0c47-103">Salva alterações criando uma confirmação para a configuração atual.</span><span class="sxs-lookup"><span data-stu-id="c0c47-103">Saves changes by creating a commit for current configuration.</span></span>

## <span data-ttu-id="c0c47-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0c47-104">SYNTAX</span></span>

```
Save-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0c47-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c0c47-105">DESCRIPTION</span></span>
<span data-ttu-id="c0c47-106">O cmdlet **Save-AzApiManagementTenantGitConfiguration** salva as alterações criando uma confirmação que contém o instantâneo de configuração atual para uma ramificação no repositório.</span><span class="sxs-lookup"><span data-stu-id="c0c47-106">The **Save-AzApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="c0c47-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0c47-107">EXAMPLES</span></span>

### <span data-ttu-id="c0c47-108">Exemplo 1: salvar alterações na configuração</span><span class="sxs-lookup"><span data-stu-id="c0c47-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="c0c47-109">Esse comando salva as alterações criando uma confirmação com o instantâneo de configuração atual para o Branch especificado no repositório.</span><span class="sxs-lookup"><span data-stu-id="c0c47-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="c0c47-110">OS</span><span class="sxs-lookup"><span data-stu-id="c0c47-110">PARAMETERS</span></span>

### <span data-ttu-id="c0c47-111">-Ramificação</span><span class="sxs-lookup"><span data-stu-id="c0c47-111">-Branch</span></span>
<span data-ttu-id="c0c47-112">Especifica o nome da ramificação git na qual confirmar o instantâneo de configuração atual.</span><span class="sxs-lookup"><span data-stu-id="c0c47-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="c0c47-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="c0c47-113">-Context</span></span>
<span data-ttu-id="c0c47-114">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c0c47-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c0c47-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0c47-115">-DefaultProfile</span></span>
<span data-ttu-id="c0c47-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c0c47-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0c47-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c0c47-117">-Force</span></span>
<span data-ttu-id="c0c47-118">Especifica que esse cmdlet confirme o banco de dados de configuração atual para o repositório do git, mesmo se o repositório do git tiver alterações mais recentes que foram sobrescritas.</span><span class="sxs-lookup"><span data-stu-id="c0c47-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="c0c47-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0c47-119">-PassThru</span></span>
<span data-ttu-id="c0c47-120">Indica que esse cmdlet retorna um objeto **PsApiManagementOperationResult** .</span><span class="sxs-lookup"><span data-stu-id="c0c47-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="c0c47-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c0c47-121">-Confirm</span></span>
<span data-ttu-id="c0c47-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0c47-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0c47-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0c47-123">-WhatIf</span></span>
<span data-ttu-id="c0c47-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c0c47-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0c47-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c0c47-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0c47-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c47-126">CommonParameters</span></span>
<span data-ttu-id="c0c47-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0c47-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c47-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0c47-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c47-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c0c47-129">INPUTS</span></span>

### <span data-ttu-id="c0c47-130">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c0c47-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c0c47-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c0c47-131">System.String</span></span>

### <span data-ttu-id="c0c47-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c0c47-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c0c47-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c0c47-133">OUTPUTS</span></span>

### <span data-ttu-id="c0c47-134">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="c0c47-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="c0c47-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c0c47-135">NOTES</span></span>

## <span data-ttu-id="c0c47-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0c47-136">RELATED LINKS</span></span>

[<span data-ttu-id="c0c47-137">Publicar-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0c47-137">Publish-AzApiManagementTenantGitConfiguration</span></span>](./Publish-AzApiManagementTenantGitConfiguration.md)


