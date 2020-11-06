---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
ms.openlocfilehash: 89d81387f8a97fe02f607ddc9d13d4645fc9688b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430367"
---
# <span data-ttu-id="97d6f-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="97d6f-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="97d6f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="97d6f-103">Comando executar na VM.</span><span class="sxs-lookup"><span data-stu-id="97d6f-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97d6f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97d6f-104">SYNTAX</span></span>

### <span data-ttu-id="97d6f-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="97d6f-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97d6f-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="97d6f-106">ResourceIdParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="97d6f-107">VMParameter</span><span class="sxs-lookup"><span data-stu-id="97d6f-107">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97d6f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="97d6f-108">DESCRIPTION</span></span>
<span data-ttu-id="97d6f-109">Invocar um comando executar na VM.</span><span class="sxs-lookup"><span data-stu-id="97d6f-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="97d6f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97d6f-110">EXAMPLES</span></span>

### <span data-ttu-id="97d6f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="97d6f-111">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="97d6f-112">Invocar um comando de execução do RunPowerShellScript com a substituição do script ' sample.ps1 ' e os parâmetros na VM de ' vmname ' no grupo de recursos ' rgname '.</span><span class="sxs-lookup"><span data-stu-id="97d6f-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="97d6f-113">OS</span><span class="sxs-lookup"><span data-stu-id="97d6f-113">PARAMETERS</span></span>

### <span data-ttu-id="97d6f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97d6f-114">-AsJob</span></span>
<span data-ttu-id="97d6f-115">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="97d6f-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="97d6f-116">-CommandId</span><span class="sxs-lookup"><span data-stu-id="97d6f-116">-CommandId</span></span>
<span data-ttu-id="97d6f-117">A ID do comando Run.</span><span class="sxs-lookup"><span data-stu-id="97d6f-117">The run command id.</span></span>

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

### <span data-ttu-id="97d6f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97d6f-118">-DefaultProfile</span></span>
<span data-ttu-id="97d6f-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="97d6f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97d6f-120">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="97d6f-120">-Parameter</span></span>
<span data-ttu-id="97d6f-121">Os parâmetros do comando Run.</span><span class="sxs-lookup"><span data-stu-id="97d6f-121">The run command parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97d6f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97d6f-122">-ResourceGroupName</span></span>
<span data-ttu-id="97d6f-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="97d6f-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97d6f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97d6f-124">-ResourceId</span></span>
<span data-ttu-id="97d6f-125">A ID do recurso da VM</span><span class="sxs-lookup"><span data-stu-id="97d6f-125">The resource id for the VM</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97d6f-126">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="97d6f-126">-ScriptPath</span></span>
<span data-ttu-id="97d6f-127">Caminho do script a ser executado.</span><span class="sxs-lookup"><span data-stu-id="97d6f-127">Path of the script to be executed.</span></span>  <span data-ttu-id="97d6f-128">Quando esse valor for fornecido, o script fornecido substituirá o script padrão do comando.</span><span class="sxs-lookup"><span data-stu-id="97d6f-128">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="97d6f-129">-VM</span><span class="sxs-lookup"><span data-stu-id="97d6f-129">-VM</span></span>
<span data-ttu-id="97d6f-130">O objeto da máquina virtual PS.</span><span class="sxs-lookup"><span data-stu-id="97d6f-130">The PS virtual Machine Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameter
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97d6f-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="97d6f-131">-VMName</span></span>
<span data-ttu-id="97d6f-132">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="97d6f-132">The name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97d6f-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="97d6f-133">-Confirm</span></span>
<span data-ttu-id="97d6f-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97d6f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97d6f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97d6f-135">-WhatIf</span></span>
<span data-ttu-id="97d6f-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="97d6f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97d6f-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="97d6f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97d6f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97d6f-138">CommonParameters</span></span>
<span data-ttu-id="97d6f-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97d6f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97d6f-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97d6f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97d6f-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="97d6f-141">INPUTS</span></span>

### <span data-ttu-id="97d6f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="97d6f-142">System.String</span></span>

### <span data-ttu-id="97d6f-143">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="97d6f-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="97d6f-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="97d6f-144">OUTPUTS</span></span>

### <span data-ttu-id="97d6f-145">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="97d6f-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="97d6f-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="97d6f-146">NOTES</span></span>

## <span data-ttu-id="97d6f-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97d6f-147">RELATED LINKS</span></span>