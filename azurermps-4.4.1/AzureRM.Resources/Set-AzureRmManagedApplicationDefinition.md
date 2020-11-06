---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 4dc41f7510789664b5c453285ebea032c24f3ac7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427794"
---
# <span data-ttu-id="82c14-101">Set-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="82c14-101">Set-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="82c14-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="82c14-102">SYNOPSIS</span></span>
<span data-ttu-id="82c14-103">Atualiza a definição do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="82c14-103">Updates managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82c14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82c14-104">SYNTAX</span></span>

### <span data-ttu-id="82c14-105">O conjunto de parâmetros do nome da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="82c14-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="82c14-106">Assume</span><span class="sxs-lookup"><span data-stu-id="82c14-106">(Default)</span></span>
```
Set-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82c14-107">O conjunto de parâmetros de ID de definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="82c14-107">The managed application definition Id parameter set.</span></span>
```
Set-AzureRmManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82c14-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="82c14-108">DESCRIPTION</span></span>
<span data-ttu-id="82c14-109">O cmdlet **set-AzureRmManagedApplicationDefinition** atualiza as definições do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="82c14-109">The **Set-AzureRmManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="82c14-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="82c14-110">EXAMPLES</span></span>

### <span data-ttu-id="82c14-111">Exemplo 1: atualizar descrição da definição do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="82c14-111">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="82c14-112">Este comando atualiza a descrição da definição do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="82c14-112">This command updates the managed application definition description</span></span>

## <span data-ttu-id="82c14-113">OS</span><span class="sxs-lookup"><span data-stu-id="82c14-113">PARAMETERS</span></span>

### <span data-ttu-id="82c14-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="82c14-114">-ApiVersion</span></span>
<span data-ttu-id="82c14-115">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="82c14-115">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="82c14-116">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="82c14-116">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82c14-117">-Authorization</span><span class="sxs-lookup"><span data-stu-id="82c14-117">-Authorization</span></span>
<span data-ttu-id="82c14-118">A autorização da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="82c14-118">The managed application definition authorization.</span></span>
<span data-ttu-id="82c14-119">Pares de autorização separados por vírgula em um formato de \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="82c14-119">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c14-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82c14-120">-DefaultProfile</span></span>
<span data-ttu-id="82c14-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="82c14-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82c14-122">-Descrição</span><span class="sxs-lookup"><span data-stu-id="82c14-122">-Description</span></span>
<span data-ttu-id="82c14-123">A descrição da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="82c14-123">The managed application definition description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c14-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="82c14-124">-DisplayName</span></span>
<span data-ttu-id="82c14-125">O nome de exibição da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="82c14-125">The managed application definition display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c14-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="82c14-126">-Name</span></span>
<span data-ttu-id="82c14-127">O nome da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="82c14-127">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c14-128">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="82c14-128">-PackageFileUri</span></span>
<span data-ttu-id="82c14-129">O URI do arquivo do pacote de definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="82c14-129">The managed application definition package file uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c14-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="82c14-130">-Pre</span></span>
<span data-ttu-id="82c14-131">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="82c14-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82c14-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82c14-132">-ResourceGroupName</span></span>
<span data-ttu-id="82c14-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="82c14-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c14-134">-Marca</span><span class="sxs-lookup"><span data-stu-id="82c14-134">-Tag</span></span>
<span data-ttu-id="82c14-135">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="82c14-135">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c14-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="82c14-136">-Confirm</span></span>
<span data-ttu-id="82c14-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82c14-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82c14-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82c14-138">-WhatIf</span></span>
<span data-ttu-id="82c14-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="82c14-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82c14-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="82c14-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82c14-141">-ID</span><span class="sxs-lookup"><span data-stu-id="82c14-141">-Id</span></span>
<span data-ttu-id="82c14-142">A ID da definição do aplicativo gerenciado totalmente qualificado, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="82c14-142">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="82c14-143">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="82c14-143">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c14-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82c14-144">CommonParameters</span></span>
<span data-ttu-id="82c14-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82c14-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82c14-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82c14-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82c14-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="82c14-147">INPUTS</span></span>

### <span data-ttu-id="82c14-148">System. String</span><span class="sxs-lookup"><span data-stu-id="82c14-148">System.String</span></span>
<span data-ttu-id="82c14-149">System. String [] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="82c14-149">System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="82c14-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="82c14-150">OUTPUTS</span></span>

### <span data-ttu-id="82c14-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="82c14-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="82c14-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="82c14-152">NOTES</span></span>

## <span data-ttu-id="82c14-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="82c14-153">RELATED LINKS</span></span>

