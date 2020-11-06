---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 8914b6d48b14ea372f29a6b7b0f5c9a1c32a6fd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426618"
---
# <span data-ttu-id="64916-101">Set-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="64916-101">Set-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="64916-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64916-102">SYNOPSIS</span></span>
<span data-ttu-id="64916-103">Atualiza a definição do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="64916-103">Updates managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64916-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64916-104">SYNTAX</span></span>

### <span data-ttu-id="64916-105">SetByNameAndResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="64916-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64916-106">SetById</span><span class="sxs-lookup"><span data-stu-id="64916-106">SetById</span></span>
```
Set-AzureRmManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64916-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64916-107">DESCRIPTION</span></span>
<span data-ttu-id="64916-108">O cmdlet **set-AzureRmManagedApplicationDefinition** atualiza as definições do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="64916-108">The **Set-AzureRmManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="64916-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64916-109">EXAMPLES</span></span>

### <span data-ttu-id="64916-110">Exemplo 1: atualizar descrição da definição do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="64916-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="64916-111">Este comando atualiza a descrição da definição do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="64916-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="64916-112">OS</span><span class="sxs-lookup"><span data-stu-id="64916-112">PARAMETERS</span></span>

### <span data-ttu-id="64916-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="64916-113">-ApiVersion</span></span>
<span data-ttu-id="64916-114">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="64916-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="64916-115">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="64916-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="64916-116">-Authorization</span><span class="sxs-lookup"><span data-stu-id="64916-116">-Authorization</span></span>
<span data-ttu-id="64916-117">A autorização da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="64916-117">The managed application definition authorization.</span></span>
<span data-ttu-id="64916-118">Pares de autorização separados por vírgula em um formato de \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="64916-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64916-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64916-119">-DefaultProfile</span></span>
<span data-ttu-id="64916-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64916-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64916-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="64916-121">-Description</span></span>
<span data-ttu-id="64916-122">A descrição da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="64916-122">The managed application definition description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64916-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="64916-123">-DisplayName</span></span>
<span data-ttu-id="64916-124">O nome de exibição da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="64916-124">The managed application definition display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64916-125">-ID</span><span class="sxs-lookup"><span data-stu-id="64916-125">-Id</span></span>
<span data-ttu-id="64916-126">A ID da definição do aplicativo gerenciado totalmente qualificado, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="64916-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="64916-127">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64916-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64916-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="64916-128">-Name</span></span>
<span data-ttu-id="64916-129">O nome da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="64916-129">The managed application definition name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64916-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="64916-130">-PackageFileUri</span></span>
<span data-ttu-id="64916-131">O URI do arquivo do pacote de definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="64916-131">The managed application definition package file uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64916-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="64916-132">-Pre</span></span>
<span data-ttu-id="64916-133">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="64916-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="64916-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64916-134">-ResourceGroupName</span></span>
<span data-ttu-id="64916-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="64916-135">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64916-136">-Marca</span><span class="sxs-lookup"><span data-stu-id="64916-136">-Tag</span></span>
<span data-ttu-id="64916-137">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="64916-137">A hash table which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64916-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="64916-138">-Confirm</span></span>
<span data-ttu-id="64916-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64916-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64916-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64916-140">-WhatIf</span></span>
<span data-ttu-id="64916-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="64916-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64916-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="64916-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64916-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64916-143">CommonParameters</span></span>
<span data-ttu-id="64916-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64916-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64916-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64916-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64916-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64916-146">INPUTS</span></span>

### <span data-ttu-id="64916-147">System. String</span><span class="sxs-lookup"><span data-stu-id="64916-147">System.String</span></span>
<span data-ttu-id="64916-148">System. String [] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="64916-148">System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="64916-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64916-149">OUTPUTS</span></span>

### <span data-ttu-id="64916-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="64916-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="64916-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64916-151">NOTES</span></span>

## <span data-ttu-id="64916-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64916-152">RELATED LINKS</span></span>
