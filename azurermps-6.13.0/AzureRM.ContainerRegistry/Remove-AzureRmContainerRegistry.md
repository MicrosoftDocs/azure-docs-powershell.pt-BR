---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: 2235e533e999fedbb06b79548bf4e2ce8de3586a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609818"
---
# <span data-ttu-id="8919f-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8919f-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="8919f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8919f-102">SYNOPSIS</span></span>
<span data-ttu-id="8919f-103">Remove um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="8919f-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8919f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8919f-104">SYNTAX</span></span>

### <span data-ttu-id="8919f-105">NameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8919f-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8919f-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8919f-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8919f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8919f-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8919f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8919f-108">DESCRIPTION</span></span>
<span data-ttu-id="8919f-109">O cmdlet Remove-AzureRmContainerRegistry remove um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="8919f-109">The Remove-AzureRmContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="8919f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8919f-110">EXAMPLES</span></span>

### <span data-ttu-id="8919f-111">Exemplo 1: remover um registro de contêiner especificado</span><span class="sxs-lookup"><span data-stu-id="8919f-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="8919f-112">Esse comando Remove o registro do contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="8919f-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="8919f-113">OS</span><span class="sxs-lookup"><span data-stu-id="8919f-113">PARAMETERS</span></span>

### <span data-ttu-id="8919f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8919f-114">-DefaultProfile</span></span>
<span data-ttu-id="8919f-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8919f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8919f-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="8919f-116">-Name</span></span>
<span data-ttu-id="8919f-117">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="8919f-117">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8919f-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8919f-118">-PassThru</span></span>
<span data-ttu-id="8919f-119">Indica que esse cmdlet retorna true se a remoção tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8919f-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="8919f-120">-Registro</span><span class="sxs-lookup"><span data-stu-id="8919f-120">-Registry</span></span>
<span data-ttu-id="8919f-121">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="8919f-121">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8919f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8919f-122">-ResourceGroupName</span></span>
<span data-ttu-id="8919f-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8919f-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8919f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8919f-124">-ResourceId</span></span>
<span data-ttu-id="8919f-125">A ID do recurso do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="8919f-125">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8919f-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8919f-126">-Confirm</span></span>
<span data-ttu-id="8919f-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8919f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8919f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8919f-128">-WhatIf</span></span>
<span data-ttu-id="8919f-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8919f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8919f-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8919f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8919f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8919f-131">CommonParameters</span></span>
<span data-ttu-id="8919f-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8919f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8919f-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8919f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8919f-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8919f-134">INPUTS</span></span>

### <span data-ttu-id="8919f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="8919f-135">System.String</span></span>

## <span data-ttu-id="8919f-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8919f-136">OUTPUTS</span></span>

### <span data-ttu-id="8919f-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8919f-137">System.Boolean</span></span>

## <span data-ttu-id="8919f-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8919f-138">NOTES</span></span>

## <span data-ttu-id="8919f-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8919f-139">RELATED LINKS</span></span>

[<span data-ttu-id="8919f-140">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8919f-140">New-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="8919f-141">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8919f-141">Get-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="8919f-142">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8919f-142">Update-AzureRmContainerRegistry</span></span>]()

