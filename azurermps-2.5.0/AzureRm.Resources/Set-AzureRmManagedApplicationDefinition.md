---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermmanagedapplicationdefinition
schema: 2.0.0
ms.openlocfilehash: ba2d158257f4be0e0daac8de5dd77e906e0abedc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785428"
---
# <span data-ttu-id="3df0d-101">Set-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="3df0d-101">Set-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="3df0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3df0d-102">SYNOPSIS</span></span>
<span data-ttu-id="3df0d-103">Atualiza a definição do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="3df0d-103">Updates managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3df0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3df0d-104">SYNTAX</span></span>

### <span data-ttu-id="3df0d-105">SetByNameAndResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="3df0d-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3df0d-106">SetById</span><span class="sxs-lookup"><span data-stu-id="3df0d-106">SetById</span></span>
```
Set-AzureRmManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3df0d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3df0d-107">DESCRIPTION</span></span>
<span data-ttu-id="3df0d-108">O cmdlet **set-AzureRmManagedApplicationDefinition** atualiza as definições do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="3df0d-108">The **Set-AzureRmManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="3df0d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3df0d-109">EXAMPLES</span></span>

### <span data-ttu-id="3df0d-110">Exemplo 1: atualizar descrição da definição do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="3df0d-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="3df0d-111">Este comando atualiza a descrição da definição do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="3df0d-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="3df0d-112">OS</span><span class="sxs-lookup"><span data-stu-id="3df0d-112">PARAMETERS</span></span>

### <span data-ttu-id="3df0d-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3df0d-113">-ApiVersion</span></span>
<span data-ttu-id="3df0d-114">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="3df0d-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="3df0d-115">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="3df0d-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="3df0d-116">-Authorization</span><span class="sxs-lookup"><span data-stu-id="3df0d-116">-Authorization</span></span>
<span data-ttu-id="3df0d-117">A autorização da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="3df0d-117">The managed application definition authorization.</span></span>
<span data-ttu-id="3df0d-118">Pares de autorização separados por vírgula em um formato de \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="3df0d-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="3df0d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3df0d-119">-DefaultProfile</span></span>
<span data-ttu-id="3df0d-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3df0d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3df0d-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="3df0d-121">-Description</span></span>
<span data-ttu-id="3df0d-122">A descrição da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="3df0d-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="3df0d-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3df0d-123">-DisplayName</span></span>
<span data-ttu-id="3df0d-124">O nome de exibição da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="3df0d-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="3df0d-125">-ID</span><span class="sxs-lookup"><span data-stu-id="3df0d-125">-Id</span></span>
<span data-ttu-id="3df0d-126">A ID da definição do aplicativo gerenciado totalmente qualificado, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="3df0d-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="3df0d-127">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3df0d-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

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

### <span data-ttu-id="3df0d-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="3df0d-128">-Name</span></span>
<span data-ttu-id="3df0d-129">O nome da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="3df0d-129">The managed application definition name.</span></span>

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

### <span data-ttu-id="3df0d-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="3df0d-130">-PackageFileUri</span></span>
<span data-ttu-id="3df0d-131">O URI do arquivo do pacote de definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="3df0d-131">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="3df0d-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="3df0d-132">-Pre</span></span>
<span data-ttu-id="3df0d-133">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="3df0d-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3df0d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3df0d-134">-ResourceGroupName</span></span>
<span data-ttu-id="3df0d-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3df0d-135">The resource group name.</span></span>

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

### <span data-ttu-id="3df0d-136">-Marca</span><span class="sxs-lookup"><span data-stu-id="3df0d-136">-Tag</span></span>
<span data-ttu-id="3df0d-137">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="3df0d-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="3df0d-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3df0d-138">-Confirm</span></span>
<span data-ttu-id="3df0d-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3df0d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3df0d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3df0d-140">-WhatIf</span></span>
<span data-ttu-id="3df0d-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3df0d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3df0d-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3df0d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3df0d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3df0d-143">CommonParameters</span></span>
<span data-ttu-id="3df0d-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3df0d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3df0d-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3df0d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3df0d-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3df0d-146">INPUTS</span></span>

### <span data-ttu-id="3df0d-147">System. String</span><span class="sxs-lookup"><span data-stu-id="3df0d-147">System.String</span></span>
<span data-ttu-id="3df0d-148">System. String [] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3df0d-148">System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="3df0d-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3df0d-149">OUTPUTS</span></span>

### <span data-ttu-id="3df0d-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="3df0d-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3df0d-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3df0d-151">NOTES</span></span>

## <span data-ttu-id="3df0d-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3df0d-152">RELATED LINKS</span></span>
