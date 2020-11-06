---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 5574966734c3b35bd5b104addf1872a85eb9660b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429685"
---
# <span data-ttu-id="f2635-101">New-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="f2635-101">New-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="f2635-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2635-102">SYNOPSIS</span></span>
<span data-ttu-id="f2635-103">Cria uma definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f2635-103">Creates a managed application definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2635-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2635-104">SYNTAX</span></span>

```
New-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2635-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f2635-105">DESCRIPTION</span></span>
<span data-ttu-id="f2635-106">O cmdlet **New-AzureRmManagedApplicationDefinition** cria uma definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f2635-106">The **New-AzureRmManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="f2635-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2635-107">EXAMPLES</span></span>

### <span data-ttu-id="f2635-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f2635-108">Example 1</span></span>
```
PS> New-AzureRmManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="f2635-109">Esse comando cria uma definição de aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="f2635-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="f2635-110">OS</span><span class="sxs-lookup"><span data-stu-id="f2635-110">PARAMETERS</span></span>

### <span data-ttu-id="f2635-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f2635-111">-ApiVersion</span></span>
<span data-ttu-id="f2635-112">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="f2635-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f2635-113">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="f2635-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f2635-114">-Authorization</span><span class="sxs-lookup"><span data-stu-id="f2635-114">-Authorization</span></span>
<span data-ttu-id="f2635-115">A autorização da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f2635-115">The managed application definition authorization.</span></span>
<span data-ttu-id="f2635-116">Pares de autorização separados por vírgula em um formato de \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="f2635-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2635-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="f2635-117">-CreateUiDefinition</span></span>
<span data-ttu-id="f2635-118">A definição de aplicativo gerenciado criar definição da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="f2635-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="f2635-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2635-119">-DefaultProfile</span></span>
<span data-ttu-id="f2635-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2635-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2635-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="f2635-121">-Description</span></span>
<span data-ttu-id="f2635-122">A descrição da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f2635-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="f2635-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f2635-123">-DisplayName</span></span>
<span data-ttu-id="f2635-124">O nome de exibição da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f2635-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="f2635-125">-Local</span><span class="sxs-lookup"><span data-stu-id="f2635-125">-Location</span></span>
<span data-ttu-id="f2635-126">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="f2635-126">The resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2635-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="f2635-127">-LockLevel</span></span>
<span data-ttu-id="f2635-128">O nível do bloqueio para a definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f2635-128">The level of the lock for managed application definition.</span></span>

```yaml
Type: ApplicationLockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2635-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="f2635-129">-MainTemplate</span></span>
<span data-ttu-id="f2635-130">O modelo principal de definição do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="f2635-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="f2635-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2635-131">-Name</span></span>
<span data-ttu-id="f2635-132">O nome da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f2635-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="f2635-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="f2635-133">-PackageFileUri</span></span>
<span data-ttu-id="f2635-134">O URI do arquivo do pacote de definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f2635-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="f2635-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="f2635-135">-Pre</span></span>
<span data-ttu-id="f2635-136">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="f2635-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f2635-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2635-137">-ResourceGroupName</span></span>
<span data-ttu-id="f2635-138">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f2635-138">The resource group name.</span></span>

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

### <span data-ttu-id="f2635-139">-Marca</span><span class="sxs-lookup"><span data-stu-id="f2635-139">-Tag</span></span>
<span data-ttu-id="f2635-140">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="f2635-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f2635-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f2635-141">-Confirm</span></span>
<span data-ttu-id="f2635-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2635-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2635-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2635-143">-WhatIf</span></span>
<span data-ttu-id="f2635-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f2635-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2635-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f2635-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2635-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2635-146">CommonParameters</span></span>
<span data-ttu-id="f2635-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2635-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2635-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2635-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2635-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f2635-149">INPUTS</span></span>

### <span data-ttu-id="f2635-150">System. String</span><span class="sxs-lookup"><span data-stu-id="f2635-150">System.String</span></span>
<span data-ttu-id="f2635-151">Microsoft. Azure. Commands. ResourceManager. cmdlets. Entities. Application. ApplicationLockLevel System. String [] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f2635-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="f2635-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f2635-152">OUTPUTS</span></span>

### <span data-ttu-id="f2635-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f2635-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f2635-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f2635-154">NOTES</span></span>

## <span data-ttu-id="f2635-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2635-155">RELATED LINKS</span></span>
