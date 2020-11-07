---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvm
schema: 2.0.0
ms.openlocfilehash: 04110cb46d3f0ed0e5e09e6b12544b927cf6ae25
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785946"
---
# <span data-ttu-id="cb884-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cb884-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="cb884-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cb884-102">SYNOPSIS</span></span>
<span data-ttu-id="cb884-103">Inicia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="cb884-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb884-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb884-104">SYNTAX</span></span>

### <span data-ttu-id="cb884-105">ResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="cb884-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb884-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="cb884-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb884-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cb884-107">DESCRIPTION</span></span>
<span data-ttu-id="cb884-108">O cmdlet **Start-AzureRmVM** inicia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="cb884-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="cb884-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cb884-109">EXAMPLES</span></span>

### <span data-ttu-id="cb884-110">Exemplo 1: iniciar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="cb884-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="cb884-111">Esse comando inicia a máquina virtual nomeada VirtualMachine07 em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="cb884-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="cb884-112">OS</span><span class="sxs-lookup"><span data-stu-id="cb884-112">PARAMETERS</span></span>

### <span data-ttu-id="cb884-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb884-113">-AsJob</span></span>
<span data-ttu-id="cb884-114">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="cb884-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="cb884-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb884-115">-DefaultProfile</span></span>
<span data-ttu-id="cb884-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cb884-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb884-117">-ID</span><span class="sxs-lookup"><span data-stu-id="cb884-117">-Id</span></span>
<span data-ttu-id="cb884-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cb884-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb884-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="cb884-119">-Name</span></span>
<span data-ttu-id="cb884-120">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cb884-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="cb884-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb884-121">-ResourceGroupName</span></span>
<span data-ttu-id="cb884-122">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cb884-122">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb884-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cb884-123">-Confirm</span></span>
<span data-ttu-id="cb884-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb884-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb884-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb884-125">-WhatIf</span></span>
<span data-ttu-id="cb884-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cb884-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb884-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cb884-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb884-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb884-128">CommonParameters</span></span>
<span data-ttu-id="cb884-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb884-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb884-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb884-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb884-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cb884-131">INPUTS</span></span>

### <span data-ttu-id="cb884-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="cb884-132">None</span></span>
<span data-ttu-id="cb884-133">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="cb884-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cb884-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cb884-134">OUTPUTS</span></span>

### <span data-ttu-id="cb884-135">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="cb884-135">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="cb884-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cb884-136">NOTES</span></span>

## <span data-ttu-id="cb884-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb884-137">RELATED LINKS</span></span>

[<span data-ttu-id="cb884-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cb884-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="cb884-139">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cb884-139">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="cb884-140">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cb884-140">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="cb884-141">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cb884-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="cb884-142">Parar-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cb884-142">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="cb884-143">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cb884-143">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


