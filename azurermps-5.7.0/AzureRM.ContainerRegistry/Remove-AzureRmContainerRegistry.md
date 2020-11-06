---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: df0c938db8f44ebffedc9760e4a3d33ee175ae01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431032"
---
# <span data-ttu-id="d162a-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d162a-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="d162a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d162a-102">SYNOPSIS</span></span>
<span data-ttu-id="d162a-103">Remove um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="d162a-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d162a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d162a-104">SYNTAX</span></span>

### <span data-ttu-id="d162a-105">NameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d162a-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d162a-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d162a-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d162a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d162a-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d162a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d162a-108">DESCRIPTION</span></span>
<span data-ttu-id="d162a-109">O cmdlet Remove-AzureRmContainerRegistry remove um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="d162a-109">The Remove-AzureRmContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="d162a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d162a-110">EXAMPLES</span></span>

### <span data-ttu-id="d162a-111">Exemplo 1: remover um registro de contêiner especificado</span><span class="sxs-lookup"><span data-stu-id="d162a-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="d162a-112">Esse comando Remove o registro do contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="d162a-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="d162a-113">OS</span><span class="sxs-lookup"><span data-stu-id="d162a-113">PARAMETERS</span></span>

### <span data-ttu-id="d162a-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="d162a-114">-Name</span></span>
<span data-ttu-id="d162a-115">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="d162a-115">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d162a-116">-Registro</span><span class="sxs-lookup"><span data-stu-id="d162a-116">-Registry</span></span>
<span data-ttu-id="d162a-117">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="d162a-117">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d162a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d162a-118">-ResourceGroupName</span></span>
<span data-ttu-id="d162a-119">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d162a-119">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d162a-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d162a-120">-Confirm</span></span>
<span data-ttu-id="d162a-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d162a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d162a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d162a-122">-WhatIf</span></span>
<span data-ttu-id="d162a-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d162a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d162a-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d162a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d162a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d162a-125">-DefaultProfile</span></span>
<span data-ttu-id="d162a-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d162a-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d162a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d162a-127">-ResourceId</span></span>
<span data-ttu-id="d162a-128">A ID do recurso do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="d162a-128">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d162a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d162a-129">-PassThru</span></span>
<span data-ttu-id="d162a-130">Indica que esse cmdlet retorna true se a remoção tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d162a-130">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="d162a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d162a-131">CommonParameters</span></span>
<span data-ttu-id="d162a-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d162a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d162a-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d162a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d162a-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d162a-134">INPUTS</span></span>

### <span data-ttu-id="d162a-135">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d162a-135">PSContainerRegistry</span></span>
<span data-ttu-id="d162a-136">O parâmetro ' Registry ' aceita o valor do tipo ' PSContainerRegistry ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="d162a-136">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="d162a-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d162a-137">OUTPUTS</span></span>

### <span data-ttu-id="d162a-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d162a-138">None</span></span>

## <span data-ttu-id="d162a-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d162a-139">NOTES</span></span>

## <span data-ttu-id="d162a-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d162a-140">RELATED LINKS</span></span>

[<span data-ttu-id="d162a-141">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d162a-141">New-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="d162a-142">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d162a-142">Get-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="d162a-143">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d162a-143">Update-AzureRmContainerRegistry</span></span>]()

