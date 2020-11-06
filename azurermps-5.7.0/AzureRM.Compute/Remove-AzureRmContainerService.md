---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
ms.openlocfilehash: da4f9846f8fceaaecc6d4385374f6525d3243e3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427612"
---
# <span data-ttu-id="e6a19-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e6a19-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="e6a19-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6a19-102">SYNOPSIS</span></span>
<span data-ttu-id="e6a19-103">Remove um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="e6a19-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6a19-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6a19-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6a19-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e6a19-105">DESCRIPTION</span></span>
<span data-ttu-id="e6a19-106">O cmdlet **Remove-AzureRmContainerService** remove um serviço de contêiner da sua conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="e6a19-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="e6a19-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e6a19-107">EXAMPLES</span></span>

### <span data-ttu-id="e6a19-108">Exemplo 1: remover um serviço de contêiner</span><span class="sxs-lookup"><span data-stu-id="e6a19-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="e6a19-109">Esse comando Remove o serviço de contêiner chamado CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="e6a19-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="e6a19-110">OS</span><span class="sxs-lookup"><span data-stu-id="e6a19-110">PARAMETERS</span></span>

### <span data-ttu-id="e6a19-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e6a19-111">-Force</span></span>
<span data-ttu-id="e6a19-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e6a19-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6a19-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6a19-113">-Name</span></span>
<span data-ttu-id="e6a19-114">Especifica o nome do serviço de contêiner que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="e6a19-114">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6a19-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6a19-115">-ResourceGroupName</span></span>
<span data-ttu-id="e6a19-116">Especifica o grupo de recursos do serviço de contêiner que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="e6a19-116">Specifies the resource group of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6a19-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e6a19-117">-Confirm</span></span>
<span data-ttu-id="e6a19-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6a19-118">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="e6a19-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6a19-119">-WhatIf</span></span>
<span data-ttu-id="e6a19-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e6a19-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6a19-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e6a19-121">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="e6a19-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6a19-122">CommonParameters</span></span>
<span data-ttu-id="e6a19-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6a19-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6a19-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6a19-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6a19-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e6a19-125">INPUTS</span></span>

### <span data-ttu-id="e6a19-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e6a19-126">None</span></span>
<span data-ttu-id="e6a19-127">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e6a19-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e6a19-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e6a19-128">OUTPUTS</span></span>

## <span data-ttu-id="e6a19-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e6a19-129">NOTES</span></span>

## <span data-ttu-id="e6a19-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6a19-130">RELATED LINKS</span></span>

[<span data-ttu-id="e6a19-131">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e6a19-131">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="e6a19-132">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e6a19-132">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="e6a19-133">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e6a19-133">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


