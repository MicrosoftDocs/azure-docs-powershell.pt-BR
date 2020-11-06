---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 91cd7855b832a406fdd3ce9a959135936ee3c284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440230"
---
# <span data-ttu-id="b0094-101">Save-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="b0094-101">Save-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="b0094-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0094-102">SYNOPSIS</span></span>
<span data-ttu-id="b0094-103">Salva alterações criando uma confirmação para a configuração atual.</span><span class="sxs-lookup"><span data-stu-id="b0094-103">Saves changes by creating a commit for current configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0094-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0094-104">SYNTAX</span></span>

```
Save-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0094-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0094-105">DESCRIPTION</span></span>
<span data-ttu-id="b0094-106">O cmdlet **Save-AzureRmApiManagementTenantGitConfiguration** salva as alterações criando uma confirmação que contém o instantâneo de configuração atual para uma ramificação no repositório.</span><span class="sxs-lookup"><span data-stu-id="b0094-106">The **Save-AzureRmApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="b0094-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0094-107">EXAMPLES</span></span>

### <span data-ttu-id="b0094-108">Exemplo 1: salvar alterações na configuração</span><span class="sxs-lookup"><span data-stu-id="b0094-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>Save-AzureRmApiManagementTenantGitConfiguration -Context $ApimContext -Branch 'master' -PassThru
```

<span data-ttu-id="b0094-109">Esse comando salva as alterações criando uma confirmação com o instantâneo de configuração atual para o Branch especificado no repositório.</span><span class="sxs-lookup"><span data-stu-id="b0094-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="b0094-110">OS</span><span class="sxs-lookup"><span data-stu-id="b0094-110">PARAMETERS</span></span>

### <span data-ttu-id="b0094-111">-Ramificação</span><span class="sxs-lookup"><span data-stu-id="b0094-111">-Branch</span></span>
<span data-ttu-id="b0094-112">Especifica o nome da ramificação git na qual confirmar o instantâneo de configuração atual.</span><span class="sxs-lookup"><span data-stu-id="b0094-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="b0094-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="b0094-113">-Context</span></span>
<span data-ttu-id="b0094-114">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="b0094-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b0094-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b0094-115">-Force</span></span>
<span data-ttu-id="b0094-116">Especifica que esse cmdlet confirme o banco de dados de configuração atual para o repositório do git, mesmo se o repositório do git tiver alterações mais recentes que foram sobrescritas.</span><span class="sxs-lookup"><span data-stu-id="b0094-116">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="b0094-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0094-117">-PassThru</span></span>
<span data-ttu-id="b0094-118">Indica que esse cmdlet retorna um objeto **PsApiManagementOperationResult** .</span><span class="sxs-lookup"><span data-stu-id="b0094-118">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="b0094-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b0094-119">-Confirm</span></span>
<span data-ttu-id="b0094-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0094-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0094-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0094-121">-WhatIf</span></span>
<span data-ttu-id="b0094-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b0094-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0094-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b0094-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0094-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0094-124">-DefaultProfile</span></span>
<span data-ttu-id="b0094-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0094-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0094-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0094-126">CommonParameters</span></span>
<span data-ttu-id="b0094-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0094-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0094-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0094-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0094-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0094-129">INPUTS</span></span>

## <span data-ttu-id="b0094-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0094-130">OUTPUTS</span></span>

### <span data-ttu-id="b0094-131">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="b0094-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="b0094-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0094-132">NOTES</span></span>

## <span data-ttu-id="b0094-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0094-133">RELATED LINKS</span></span>

[<span data-ttu-id="b0094-134">Publicar-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="b0094-134">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>](./Publish-AzureRmApiManagementTenantGitConfiguration.md)


