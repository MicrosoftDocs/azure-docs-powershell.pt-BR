---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 32e633d1f9fea877ef81b6c6e7ef5e8bb09da81a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260431"
---
# <span data-ttu-id="971f0-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="971f0-101">Start-AzVM</span></span>

## <span data-ttu-id="971f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="971f0-102">SYNOPSIS</span></span>
<span data-ttu-id="971f0-103">Inicia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="971f0-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="971f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="971f0-104">SYNTAX</span></span>

### <span data-ttu-id="971f0-105">ResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="971f0-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="971f0-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="971f0-106">IdParameterSetName</span></span>
```
Start-AzVM [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="971f0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="971f0-107">DESCRIPTION</span></span>
<span data-ttu-id="971f0-108">O cmdlet **Start-AzVM** inicia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="971f0-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="971f0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="971f0-109">EXAMPLES</span></span>

### <span data-ttu-id="971f0-110">Exemplo 1: iniciar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="971f0-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="971f0-111">Esse comando inicia a máquina virtual nomeada VirtualMachine07 em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="971f0-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="971f0-112">OS</span><span class="sxs-lookup"><span data-stu-id="971f0-112">PARAMETERS</span></span>

### <span data-ttu-id="971f0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="971f0-113">-AsJob</span></span>
<span data-ttu-id="971f0-114">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="971f0-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="971f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="971f0-115">-DefaultProfile</span></span>
<span data-ttu-id="971f0-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="971f0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="971f0-117">-ID</span><span class="sxs-lookup"><span data-stu-id="971f0-117">-Id</span></span>
<span data-ttu-id="971f0-118">A ID da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="971f0-118">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="971f0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="971f0-119">-Name</span></span>
<span data-ttu-id="971f0-120">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="971f0-120">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971f0-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="971f0-121">-NoWait</span></span>
<span data-ttu-id="971f0-122">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="971f0-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="971f0-123">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="971f0-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="971f0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="971f0-124">-ResourceGroupName</span></span>
<span data-ttu-id="971f0-125">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="971f0-125">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="971f0-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="971f0-126">-Confirm</span></span>
<span data-ttu-id="971f0-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="971f0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="971f0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="971f0-128">-WhatIf</span></span>
<span data-ttu-id="971f0-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="971f0-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="971f0-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="971f0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="971f0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="971f0-131">CommonParameters</span></span>
<span data-ttu-id="971f0-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="971f0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="971f0-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="971f0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="971f0-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="971f0-134">INPUTS</span></span>

### <span data-ttu-id="971f0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="971f0-135">System.String</span></span>

## <span data-ttu-id="971f0-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="971f0-136">OUTPUTS</span></span>

### <span data-ttu-id="971f0-137">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="971f0-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="971f0-138">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="971f0-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="971f0-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="971f0-139">NOTES</span></span>

## <span data-ttu-id="971f0-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="971f0-140">RELATED LINKS</span></span>

[<span data-ttu-id="971f0-141">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="971f0-141">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="971f0-142">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="971f0-142">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="971f0-143">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="971f0-143">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="971f0-144">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="971f0-144">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="971f0-145">Parar-AzVM</span><span class="sxs-lookup"><span data-stu-id="971f0-145">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="971f0-146">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="971f0-146">Update-AzVM</span></span>](./Update-AzVM.md)


