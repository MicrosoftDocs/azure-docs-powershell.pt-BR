---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
ms.openlocfilehash: 84d3f73735c3606813d769d9b0daf0f9716fc1a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115598"
---
# <span data-ttu-id="517ab-101">Stop-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="517ab-101">Stop-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="517ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="517ab-102">SYNOPSIS</span></span>
<span data-ttu-id="517ab-103">Cancela uma instrução Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="517ab-103">Cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="517ab-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="517ab-104">SYNTAX</span></span>

### <span data-ttu-id="517ab-105">StopSparkStatementByIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="517ab-105">StopSparkStatementByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> -SessionId <Int32>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="517ab-106">StopSparkStatementByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="517ab-106">StopSparkStatementByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="517ab-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="517ab-107">DESCRIPTION</span></span>
<span data-ttu-id="517ab-108">O cmdlet **Stop-AzSynapseSparkStatement** cancela uma instrução Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="517ab-108">The **Stop-AzSynapseSparkStatement** cmdlet cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="517ab-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="517ab-109">EXAMPLES</span></span>

### <span data-ttu-id="517ab-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="517ab-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 130 -LivyId 1
```

<span data-ttu-id="517ab-111">Esse comando cancela a instrução Spark com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="517ab-111">This command cancels the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="517ab-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="517ab-112">Example 2</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $session | Stop-AzSynapseStatement -LivyId 3
```

<span data-ttu-id="517ab-113">Esse comando cancela a instrução Spark com a ID especificada através do pipeline.</span><span class="sxs-lookup"><span data-stu-id="517ab-113">This command cancels the Spark statement with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="517ab-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="517ab-114">PARAMETERS</span></span>

### <span data-ttu-id="517ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="517ab-115">-DefaultProfile</span></span>
<span data-ttu-id="517ab-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="517ab-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="517ab-117">-Forçar</span><span class="sxs-lookup"><span data-stu-id="517ab-117">-Force</span></span>
<span data-ttu-id="517ab-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="517ab-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="517ab-119">-Ela</span><span class="sxs-lookup"><span data-stu-id="517ab-119">-LivyId</span></span>
<span data-ttu-id="517ab-120">Identificador da instrução Spark.</span><span class="sxs-lookup"><span data-stu-id="517ab-120">Identifier of Spark statement.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="517ab-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="517ab-121">-PassThru</span></span>
<span data-ttu-id="517ab-122">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="517ab-122">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="517ab-123">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="517ab-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="517ab-124">-SessionId</span><span class="sxs-lookup"><span data-stu-id="517ab-124">-SessionId</span></span>
<span data-ttu-id="517ab-125">Identificador da sessão do Spark.</span><span class="sxs-lookup"><span data-stu-id="517ab-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="517ab-126">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="517ab-126">-SessionObject</span></span>
<span data-ttu-id="517ab-127">Objeto de entrada de sessão de spark, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="517ab-127">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: StopSparkStatementByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="517ab-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="517ab-128">-SparkPoolName</span></span>
<span data-ttu-id="517ab-129">Nome do pool de miniapse.</span><span class="sxs-lookup"><span data-stu-id="517ab-129">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="517ab-130">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="517ab-130">-WorkspaceName</span></span>
<span data-ttu-id="517ab-131">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="517ab-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="517ab-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="517ab-132">-Confirm</span></span>
<span data-ttu-id="517ab-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="517ab-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="517ab-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="517ab-134">-WhatIf</span></span>
<span data-ttu-id="517ab-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="517ab-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="517ab-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="517ab-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="517ab-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="517ab-137">CommonParameters</span></span>
<span data-ttu-id="517ab-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="517ab-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="517ab-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="517ab-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="517ab-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="517ab-140">INPUTS</span></span>

### <span data-ttu-id="517ab-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="517ab-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="517ab-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="517ab-142">OUTPUTS</span></span>

### <span data-ttu-id="517ab-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="517ab-143">System.Boolean</span></span>

## <span data-ttu-id="517ab-144">Notas</span><span class="sxs-lookup"><span data-stu-id="517ab-144">NOTES</span></span>

## <span data-ttu-id="517ab-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="517ab-145">RELATED LINKS</span></span>
