---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
ms.openlocfilehash: 7d3c27ad8dacb288aeb0d15235aacc48405b8a6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610414"
---
# <span data-ttu-id="c0830-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="c0830-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="c0830-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c0830-102">SYNOPSIS</span></span>
<span data-ttu-id="c0830-103">Comando executar na VM.</span><span class="sxs-lookup"><span data-stu-id="c0830-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0830-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0830-104">SYNTAX</span></span>

### <span data-ttu-id="c0830-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="c0830-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0830-106">VMParameter</span><span class="sxs-lookup"><span data-stu-id="c0830-106">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0830-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c0830-107">DESCRIPTION</span></span>
<span data-ttu-id="c0830-108">Invocar um comando executar na VM.</span><span class="sxs-lookup"><span data-stu-id="c0830-108">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="c0830-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0830-109">EXAMPLES</span></span>

### <span data-ttu-id="c0830-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c0830-110">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="c0830-111">Invocar um comando de execução do RunPowerShellScript com a substituição do script ' sample.ps1 ' e os parâmetros na VM de ' vmname ' no grupo de recursos ' rgname '.</span><span class="sxs-lookup"><span data-stu-id="c0830-111">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="c0830-112">OS</span><span class="sxs-lookup"><span data-stu-id="c0830-112">PARAMETERS</span></span>

### <span data-ttu-id="c0830-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0830-113">-AsJob</span></span>
<span data-ttu-id="c0830-114">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="c0830-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c0830-115">-CommandId</span><span class="sxs-lookup"><span data-stu-id="c0830-115">-CommandId</span></span>
<span data-ttu-id="c0830-116">A ID do comando Run.</span><span class="sxs-lookup"><span data-stu-id="c0830-116">The run command id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0830-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0830-117">-DefaultProfile</span></span>
<span data-ttu-id="c0830-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c0830-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0830-119">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="c0830-119">-Parameter</span></span>
<span data-ttu-id="c0830-120">Os parâmetros do comando Run.</span><span class="sxs-lookup"><span data-stu-id="c0830-120">The run command parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0830-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0830-121">-ResourceGroupName</span></span>
<span data-ttu-id="c0830-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c0830-122">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0830-123">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="c0830-123">-ScriptPath</span></span>
<span data-ttu-id="c0830-124">Caminho do script a ser executado.</span><span class="sxs-lookup"><span data-stu-id="c0830-124">Path of the script to be executed.</span></span>  <span data-ttu-id="c0830-125">Quando esse valor for fornecido, o script fornecido substituirá o script padrão do comando.</span><span class="sxs-lookup"><span data-stu-id="c0830-125">When this value is given, the given script will override the default script of the command.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0830-126">-VM</span><span class="sxs-lookup"><span data-stu-id="c0830-126">-VM</span></span>
<span data-ttu-id="c0830-127">O objeto da máquina virtual PS.</span><span class="sxs-lookup"><span data-stu-id="c0830-127">The PS virtual Machine Object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: VMParameter
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0830-128">-VMName</span><span class="sxs-lookup"><span data-stu-id="c0830-128">-VMName</span></span>
<span data-ttu-id="c0830-129">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c0830-129">The name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0830-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c0830-130">-Confirm</span></span>
<span data-ttu-id="c0830-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0830-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0830-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0830-132">-WhatIf</span></span>
<span data-ttu-id="c0830-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c0830-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0830-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c0830-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0830-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0830-135">CommonParameters</span></span>
<span data-ttu-id="c0830-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0830-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0830-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0830-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0830-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c0830-138">INPUTS</span></span>

### <span data-ttu-id="c0830-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c0830-139">System.String</span></span>
<span data-ttu-id="c0830-140">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c0830-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c0830-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c0830-141">OUTPUTS</span></span>

### <span data-ttu-id="c0830-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="c0830-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="c0830-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c0830-143">NOTES</span></span>

## <span data-ttu-id="c0830-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0830-144">RELATED LINKS</span></span>
