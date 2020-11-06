---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/save-azurermapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 7401c359a9af82d1b65749a3276aada89ab9320d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426833"
---
# <span data-ttu-id="ab867-101">Save-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab867-101">Save-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="ab867-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab867-102">SYNOPSIS</span></span>
<span data-ttu-id="ab867-103">Salva alterações criando uma confirmação para a configuração atual.</span><span class="sxs-lookup"><span data-stu-id="ab867-103">Saves changes by creating a commit for current configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab867-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab867-104">SYNTAX</span></span>

```
Save-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab867-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ab867-105">DESCRIPTION</span></span>
<span data-ttu-id="ab867-106">O cmdlet **Save-AzureRmApiManagementTenantGitConfiguration** salva as alterações criando uma confirmação que contém o instantâneo de configuração atual para uma ramificação no repositório.</span><span class="sxs-lookup"><span data-stu-id="ab867-106">The **Save-AzureRmApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="ab867-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ab867-107">EXAMPLES</span></span>

### <span data-ttu-id="ab867-108">Exemplo 1: salvar alterações na configuração</span><span class="sxs-lookup"><span data-stu-id="ab867-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="ab867-109">Esse comando salva as alterações criando uma confirmação com o instantâneo de configuração atual para o Branch especificado no repositório.</span><span class="sxs-lookup"><span data-stu-id="ab867-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="ab867-110">OS</span><span class="sxs-lookup"><span data-stu-id="ab867-110">PARAMETERS</span></span>

### <span data-ttu-id="ab867-111">-Ramificação</span><span class="sxs-lookup"><span data-stu-id="ab867-111">-Branch</span></span>
<span data-ttu-id="ab867-112">Especifica o nome da ramificação git na qual confirmar o instantâneo de configuração atual.</span><span class="sxs-lookup"><span data-stu-id="ab867-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab867-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="ab867-113">-Context</span></span>
<span data-ttu-id="ab867-114">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ab867-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab867-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab867-115">-DefaultProfile</span></span>
<span data-ttu-id="ab867-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ab867-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab867-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ab867-117">-Force</span></span>
<span data-ttu-id="ab867-118">Especifica que esse cmdlet confirme o banco de dados de configuração atual para o repositório do git, mesmo se o repositório do git tiver alterações mais recentes que foram sobrescritas.</span><span class="sxs-lookup"><span data-stu-id="ab867-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab867-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab867-119">-PassThru</span></span>
<span data-ttu-id="ab867-120">Indica que esse cmdlet retorna um objeto **PsApiManagementOperationResult** .</span><span class="sxs-lookup"><span data-stu-id="ab867-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab867-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ab867-121">-Confirm</span></span>
<span data-ttu-id="ab867-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab867-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab867-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab867-123">-WhatIf</span></span>
<span data-ttu-id="ab867-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ab867-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab867-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ab867-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab867-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab867-126">CommonParameters</span></span>
<span data-ttu-id="ab867-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab867-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab867-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab867-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab867-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ab867-129">INPUTS</span></span>

### <span data-ttu-id="ab867-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ab867-130">None</span></span>
<span data-ttu-id="ab867-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="ab867-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ab867-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ab867-132">OUTPUTS</span></span>

### <span data-ttu-id="ab867-133">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="ab867-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="ab867-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ab867-134">NOTES</span></span>

## <span data-ttu-id="ab867-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab867-135">RELATED LINKS</span></span>

[<span data-ttu-id="ab867-136">Publicar-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab867-136">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>](./Publish-AzureRmApiManagementTenantGitConfiguration.md)


