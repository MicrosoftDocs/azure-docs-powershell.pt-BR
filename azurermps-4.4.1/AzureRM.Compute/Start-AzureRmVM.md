---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVM.md
ms.openlocfilehash: 3091cb877ff792527cf97e3d44b7c363f9dd94b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427995"
---
# <span data-ttu-id="f87eb-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f87eb-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="f87eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f87eb-102">SYNOPSIS</span></span>
<span data-ttu-id="f87eb-103">Inicia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="f87eb-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f87eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f87eb-104">SYNTAX</span></span>

### <span data-ttu-id="f87eb-105">ResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="f87eb-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f87eb-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f87eb-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f87eb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f87eb-107">DESCRIPTION</span></span>
<span data-ttu-id="f87eb-108">O cmdlet **Start-AzureRmVM** inicia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="f87eb-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="f87eb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f87eb-109">EXAMPLES</span></span>

### <span data-ttu-id="f87eb-110">Exemplo 1: iniciar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="f87eb-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="f87eb-111">Esse comando inicia a máquina virtual nomeada VirtualMachine07 em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f87eb-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="f87eb-112">OS</span><span class="sxs-lookup"><span data-stu-id="f87eb-112">PARAMETERS</span></span>

### <span data-ttu-id="f87eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f87eb-113">-DefaultProfile</span></span>
<span data-ttu-id="f87eb-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f87eb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f87eb-115">-ID</span><span class="sxs-lookup"><span data-stu-id="f87eb-115">-Id</span></span>
<span data-ttu-id="f87eb-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f87eb-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f87eb-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f87eb-117">-Name</span></span>
<span data-ttu-id="f87eb-118">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f87eb-118">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f87eb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f87eb-119">-ResourceGroupName</span></span>
<span data-ttu-id="f87eb-120">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f87eb-120">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f87eb-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f87eb-121">-Confirm</span></span>
<span data-ttu-id="f87eb-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f87eb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f87eb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f87eb-123">-WhatIf</span></span>
<span data-ttu-id="f87eb-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f87eb-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f87eb-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f87eb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f87eb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f87eb-126">CommonParameters</span></span>
<span data-ttu-id="f87eb-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f87eb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f87eb-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f87eb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f87eb-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f87eb-129">INPUTS</span></span>

## <span data-ttu-id="f87eb-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f87eb-130">OUTPUTS</span></span>

## <span data-ttu-id="f87eb-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f87eb-131">NOTES</span></span>

## <span data-ttu-id="f87eb-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f87eb-132">RELATED LINKS</span></span>

[<span data-ttu-id="f87eb-133">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f87eb-133">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="f87eb-134">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f87eb-134">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="f87eb-135">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f87eb-135">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="f87eb-136">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f87eb-136">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="f87eb-137">Parar-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f87eb-137">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="f87eb-138">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f87eb-138">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


