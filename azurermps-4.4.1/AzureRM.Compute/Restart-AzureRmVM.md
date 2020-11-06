---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVM.md
ms.openlocfilehash: 5a848c2e4a13df6a38c67e067531ff8581bd595e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426952"
---
# <span data-ttu-id="5ee63-101">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5ee63-101">Restart-AzureRmVM</span></span>

## <span data-ttu-id="5ee63-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5ee63-102">SYNOPSIS</span></span>
<span data-ttu-id="5ee63-103">Reinicia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="5ee63-103">Restarts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ee63-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ee63-104">SYNTAX</span></span>

### <span data-ttu-id="5ee63-105">RestartResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="5ee63-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ee63-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="5ee63-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ee63-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="5ee63-107">RestartIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ee63-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="5ee63-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-PerformMaintenance]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ee63-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5ee63-109">DESCRIPTION</span></span>
<span data-ttu-id="5ee63-110">O cmdlet **Restart-AzureRmVM** reinicia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="5ee63-110">The **Restart-AzureRmVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="5ee63-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5ee63-111">EXAMPLES</span></span>

### <span data-ttu-id="5ee63-112">Exemplo 1: reiniciar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="5ee63-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="5ee63-113">Esse comando reinicia a máquina virtual chamada VirtualMachine07 em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="5ee63-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="5ee63-114">OS</span><span class="sxs-lookup"><span data-stu-id="5ee63-114">PARAMETERS</span></span>

### <span data-ttu-id="5ee63-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ee63-115">-DefaultProfile</span></span>
<span data-ttu-id="5ee63-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5ee63-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ee63-117">-ID</span><span class="sxs-lookup"><span data-stu-id="5ee63-117">-Id</span></span>
<span data-ttu-id="5ee63-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5ee63-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ee63-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ee63-119">-Name</span></span>
<span data-ttu-id="5ee63-120">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5ee63-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="5ee63-121">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="5ee63-121">-PerformMaintenance</span></span>
<span data-ttu-id="5ee63-122">Para executar a manutenção da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5ee63-122">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ee63-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ee63-123">-ResourceGroupName</span></span>
<span data-ttu-id="5ee63-124">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5ee63-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ee63-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5ee63-125">-Confirm</span></span>
<span data-ttu-id="5ee63-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ee63-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ee63-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ee63-127">-WhatIf</span></span>
<span data-ttu-id="5ee63-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5ee63-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ee63-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5ee63-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ee63-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ee63-130">CommonParameters</span></span>
<span data-ttu-id="5ee63-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ee63-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ee63-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ee63-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ee63-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5ee63-133">INPUTS</span></span>

## <span data-ttu-id="5ee63-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5ee63-134">OUTPUTS</span></span>

## <span data-ttu-id="5ee63-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5ee63-135">NOTES</span></span>

## <span data-ttu-id="5ee63-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ee63-136">RELATED LINKS</span></span>

[<span data-ttu-id="5ee63-137">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5ee63-137">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="5ee63-138">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5ee63-138">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="5ee63-139">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5ee63-139">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="5ee63-140">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5ee63-140">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="5ee63-141">Parar-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5ee63-141">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="5ee63-142">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5ee63-142">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


