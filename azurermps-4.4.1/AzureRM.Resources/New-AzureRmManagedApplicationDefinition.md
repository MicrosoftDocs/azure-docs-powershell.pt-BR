---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 4a66541d870d30f2de199297417d211479ecc83b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440956"
---
# <span data-ttu-id="a05da-101">New-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="a05da-101">New-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="a05da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a05da-102">SYNOPSIS</span></span>
<span data-ttu-id="a05da-103">Cria uma definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a05da-103">Creates a managed application definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a05da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a05da-104">SYNTAX</span></span>

```
New-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a05da-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a05da-105">DESCRIPTION</span></span>
<span data-ttu-id="a05da-106">O cmdlet **New-AzureRmManagedApplicationDefinition** cria uma definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a05da-106">The **New-AzureRmManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="a05da-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a05da-107">EXAMPLES</span></span>

### <span data-ttu-id="a05da-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a05da-108">Example 1</span></span>
```
PS C:\> New-AzureRmManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName "test" -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="a05da-109">Esse comando cria uma definição de aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="a05da-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="a05da-110">OS</span><span class="sxs-lookup"><span data-stu-id="a05da-110">PARAMETERS</span></span>

### <span data-ttu-id="a05da-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a05da-111">-ApiVersion</span></span>
<span data-ttu-id="a05da-112">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="a05da-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a05da-113">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="a05da-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="a05da-114">-Authorization</span><span class="sxs-lookup"><span data-stu-id="a05da-114">-Authorization</span></span>
<span data-ttu-id="a05da-115">A autorização da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a05da-115">The managed application definition authorization.</span></span>
<span data-ttu-id="a05da-116">Pares de autorização separados por vírgula em um formato de \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="a05da-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a05da-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a05da-117">-DefaultProfile</span></span>
<span data-ttu-id="a05da-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a05da-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a05da-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="a05da-119">-Description</span></span>
<span data-ttu-id="a05da-120">A descrição da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a05da-120">The managed application definition description.</span></span>

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

### <span data-ttu-id="a05da-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a05da-121">-DisplayName</span></span>
<span data-ttu-id="a05da-122">O nome de exibição da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a05da-122">The managed application definition display name.</span></span>

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

### <span data-ttu-id="a05da-123">-Local</span><span class="sxs-lookup"><span data-stu-id="a05da-123">-Location</span></span>
<span data-ttu-id="a05da-124">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="a05da-124">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a05da-125">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="a05da-125">-LockLevel</span></span>
<span data-ttu-id="a05da-126">O nível do bloqueio para a definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a05da-126">The level of the lock for managed application definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a05da-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="a05da-127">-Name</span></span>
<span data-ttu-id="a05da-128">O nome da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a05da-128">The managed application definition name.</span></span>

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

### <span data-ttu-id="a05da-129">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="a05da-129">-PackageFileUri</span></span>
<span data-ttu-id="a05da-130">O URI do arquivo do pacote de definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a05da-130">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="a05da-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="a05da-131">-Pre</span></span>
<span data-ttu-id="a05da-132">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="a05da-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a05da-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a05da-133">-ResourceGroupName</span></span>
<span data-ttu-id="a05da-134">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a05da-134">The resource group name.</span></span>

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

### <span data-ttu-id="a05da-135">-Marca</span><span class="sxs-lookup"><span data-stu-id="a05da-135">-Tag</span></span>
<span data-ttu-id="a05da-136">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="a05da-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a05da-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a05da-137">-Confirm</span></span>
<span data-ttu-id="a05da-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a05da-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a05da-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a05da-139">-WhatIf</span></span>
<span data-ttu-id="a05da-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a05da-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a05da-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a05da-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a05da-142">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="a05da-142">-CreateUiDefinition</span></span>
<span data-ttu-id="a05da-143">A definição da interface do aplicativo gerenciada Create UI.</span><span class="sxs-lookup"><span data-stu-id="a05da-143">The managed application definition create ui definition.</span></span>

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

### <span data-ttu-id="a05da-144">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="a05da-144">-MainTemplate</span></span>
<span data-ttu-id="a05da-145">O modelo principal de definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a05da-145">The managed application definition main template.</span></span>

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

### <span data-ttu-id="a05da-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a05da-146">CommonParameters</span></span>
<span data-ttu-id="a05da-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a05da-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a05da-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a05da-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a05da-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a05da-149">INPUTS</span></span>

### <span data-ttu-id="a05da-150">System. String</span><span class="sxs-lookup"><span data-stu-id="a05da-150">System.String</span></span>
<span data-ttu-id="a05da-151">Microsoft. Azure. Commands. ResourceManager. cmdlets. Entities. Application. ApplicationLockLevel System. String [] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a05da-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="a05da-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a05da-152">OUTPUTS</span></span>

### <span data-ttu-id="a05da-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a05da-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a05da-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a05da-154">NOTES</span></span>

## <span data-ttu-id="a05da-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a05da-155">RELATED LINKS</span></span>

