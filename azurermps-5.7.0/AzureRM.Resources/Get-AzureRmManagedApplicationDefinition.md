---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 9dec17ba09bf76ec7e8f3323b7cfd0557e08e525
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432910"
---
# <span data-ttu-id="bcb29-101">Get-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="bcb29-101">Get-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="bcb29-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bcb29-102">SYNOPSIS</span></span>
<span data-ttu-id="bcb29-103">Obtém definições de aplicativos gerenciados</span><span class="sxs-lookup"><span data-stu-id="bcb29-103">Gets managed application definitions</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcb29-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bcb29-104">SYNTAX</span></span>

### <span data-ttu-id="bcb29-105">GetByNameAndResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="bcb29-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzureRmManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcb29-106">GetById</span><span class="sxs-lookup"><span data-stu-id="bcb29-106">GetById</span></span>
```
Get-AzureRmManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcb29-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bcb29-107">DESCRIPTION</span></span>
<span data-ttu-id="bcb29-108">O cmdlet **Get-AzureRmManagedApplicationDefinition** Obtém definições de aplicativos gerenciados</span><span class="sxs-lookup"><span data-stu-id="bcb29-108">The **Get-AzureRmManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="bcb29-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bcb29-109">EXAMPLES</span></span>

### <span data-ttu-id="bcb29-110">Exemplo 1: obter todas as definições de aplicativos gerenciados em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="bcb29-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="bcb29-111">Este comando obtém as definições do aplicativo gerenciado no grupo de recursos "MyRG"</span><span class="sxs-lookup"><span data-stu-id="bcb29-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="bcb29-112">Exemplo 2: obter uma definição de aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="bcb29-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="bcb29-113">Este comando obtém a definição do aplicativo gerenciado "myManagedAppDef" em grupo de recursos "MyRG"</span><span class="sxs-lookup"><span data-stu-id="bcb29-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="bcb29-114">OS</span><span class="sxs-lookup"><span data-stu-id="bcb29-114">PARAMETERS</span></span>

### <span data-ttu-id="bcb29-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bcb29-115">-ApiVersion</span></span>
<span data-ttu-id="bcb29-116">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="bcb29-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="bcb29-117">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="bcb29-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb29-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcb29-118">-DefaultProfile</span></span>
<span data-ttu-id="bcb29-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bcb29-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcb29-120">-ID</span><span class="sxs-lookup"><span data-stu-id="bcb29-120">-Id</span></span>
<span data-ttu-id="bcb29-121">A ID da definição do aplicativo gerenciado totalmente qualificado, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="bcb29-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="bcb29-122">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="bcb29-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcb29-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="bcb29-123">-Name</span></span>
<span data-ttu-id="bcb29-124">O nome da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="bcb29-124">The managed application definition name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcb29-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="bcb29-125">-Pre</span></span>
<span data-ttu-id="bcb29-126">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="bcb29-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb29-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcb29-127">-ResourceGroupName</span></span>
<span data-ttu-id="bcb29-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bcb29-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcb29-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcb29-129">CommonParameters</span></span>
<span data-ttu-id="bcb29-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcb29-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcb29-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcb29-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcb29-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bcb29-132">INPUTS</span></span>

### <span data-ttu-id="bcb29-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bcb29-133">System.String</span></span>

## <span data-ttu-id="bcb29-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bcb29-134">OUTPUTS</span></span>

### <span data-ttu-id="bcb29-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="bcb29-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="bcb29-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bcb29-136">NOTES</span></span>

## <span data-ttu-id="bcb29-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bcb29-137">RELATED LINKS</span></span>