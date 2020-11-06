---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: 5a5ea87044c18e82f4c17294356a35adb254eee4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427996"
---
# <span data-ttu-id="05801-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="05801-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="05801-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="05801-102">SYNOPSIS</span></span>
<span data-ttu-id="05801-103">Remove um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="05801-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05801-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05801-104">SYNTAX</span></span>

### <span data-ttu-id="05801-105">NameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="05801-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05801-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05801-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05801-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="05801-107">DESCRIPTION</span></span>
<span data-ttu-id="05801-108">O cmdlet **Remove-AzureRmContainerRegistry** remove um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="05801-108">The **Remove-AzureRmContainerRegistry** cmdlet removes a container registry.</span></span>

## <span data-ttu-id="05801-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="05801-109">EXAMPLES</span></span>

### <span data-ttu-id="05801-110">Exemplo 1: remover um registro de contêiner especificado</span><span class="sxs-lookup"><span data-stu-id="05801-110">Example 1: Remove a specified container registry</span></span>
```
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="05801-111">Esse comando Remove o registro do contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="05801-111">This command removes the specified container registry.</span></span>

## <span data-ttu-id="05801-112">OS</span><span class="sxs-lookup"><span data-stu-id="05801-112">PARAMETERS</span></span>

### <span data-ttu-id="05801-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="05801-113">-Name</span></span>
<span data-ttu-id="05801-114">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="05801-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="05801-115">-Registro</span><span class="sxs-lookup"><span data-stu-id="05801-115">-Registry</span></span>
<span data-ttu-id="05801-116">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="05801-116">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05801-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05801-117">-ResourceGroupName</span></span>
<span data-ttu-id="05801-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="05801-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="05801-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="05801-119">-Confirm</span></span>
<span data-ttu-id="05801-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05801-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05801-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05801-121">-WhatIf</span></span>
<span data-ttu-id="05801-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="05801-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05801-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="05801-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05801-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05801-124">-DefaultProfile</span></span>
<span data-ttu-id="05801-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="05801-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05801-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05801-126">CommonParameters</span></span>
<span data-ttu-id="05801-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05801-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05801-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05801-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05801-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="05801-129">INPUTS</span></span>

### <span data-ttu-id="05801-130">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="05801-130">PSContainerRegistry</span></span>
<span data-ttu-id="05801-131">O parâmetro ' Registry ' aceita o valor do tipo ' PSContainerRegistry ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="05801-131">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="05801-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="05801-132">OUTPUTS</span></span>

### <span data-ttu-id="05801-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="05801-133">None</span></span>

## <span data-ttu-id="05801-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="05801-134">NOTES</span></span>

## <span data-ttu-id="05801-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05801-135">RELATED LINKS</span></span>

[<span data-ttu-id="05801-136">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="05801-136">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="05801-137">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="05801-137">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="05801-138">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="05801-138">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

