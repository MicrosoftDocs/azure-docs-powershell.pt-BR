---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/resume-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
ms.openlocfilehash: 95ed2dc354f32229727a3d1b13dbfdfb95fe001a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118401"
---
# <span data-ttu-id="b5aa6-101">Resume-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="b5aa6-101">Resume-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="b5aa6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b5aa6-102">SYNOPSIS</span></span>
<span data-ttu-id="b5aa6-103">Resume/Resync a conexão no volume de destino.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-103">Resume/Resync the connection on the destination volume.</span></span> <span data-ttu-id="b5aa6-104">Se a operação for realizada no volume de origem, ela reverterá a sincronização da conexão e sincronizará da origem para o destino.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-104">If the operation is ran on the source volume it will reverse-resync the connection and sync from source to destination.</span></span>

## <span data-ttu-id="b5aa6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5aa6-105">SYNTAX</span></span>

### <span data-ttu-id="b5aa6-106">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b5aa6-106">ByFieldsParameterSet (Default)</span></span>
```
Resume-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5aa6-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5aa6-107">ByResourceIdParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5aa6-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5aa6-108">ByObjectParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5aa6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5aa6-109">DESCRIPTION</span></span>
<span data-ttu-id="b5aa6-110">Retomar/Ressync a conexão no volume de destino</span><span class="sxs-lookup"><span data-stu-id="b5aa6-110">Resume/Resync the connection on the destination volume</span></span>

## <span data-ttu-id="b5aa6-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b5aa6-111">EXAMPLES</span></span>

### <span data-ttu-id="b5aa6-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b5aa6-112">Example 1</span></span>
```powershell
PS C:\> Resume-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="b5aa6-113">Esse comando retoma a conexão de Replicação ANF no volume "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="b5aa6-113">This command resumes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="b5aa6-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5aa6-114">PARAMETERS</span></span>

### <span data-ttu-id="b5aa6-115">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="b5aa6-115">-AccountName</span></span>
<span data-ttu-id="b5aa6-116">O nome da conta ANF do volume de replicação</span><span class="sxs-lookup"><span data-stu-id="b5aa6-116">The name of the ANF account of the replication volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5aa6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5aa6-117">-DefaultProfile</span></span>
<span data-ttu-id="b5aa6-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5aa6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5aa6-119">-InputObject</span></span>
<span data-ttu-id="b5aa6-120">O objeto de volume de destino de replicação ANF para ressincron</span><span class="sxs-lookup"><span data-stu-id="b5aa6-120">The ANF replication destination volume object to resync</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5aa6-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b5aa6-121">-Name</span></span>
<span data-ttu-id="b5aa6-122">O nome do volume de destino de replicação da ANF</span><span class="sxs-lookup"><span data-stu-id="b5aa6-122">The name of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5aa6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5aa6-123">-PassThru</span></span>
<span data-ttu-id="b5aa6-124">Retornar se o ressíncrono do volume de replicação especificado foi executado</span><span class="sxs-lookup"><span data-stu-id="b5aa6-124">Return whether resync of the specified replication volume was performed</span></span>

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

### <span data-ttu-id="b5aa6-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="b5aa6-125">-PoolName</span></span>
<span data-ttu-id="b5aa6-126">O nome do pool de ANF do volume de replicação</span><span class="sxs-lookup"><span data-stu-id="b5aa6-126">The name of the ANF pool of the replication volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5aa6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5aa6-127">-ResourceGroupName</span></span>
<span data-ttu-id="b5aa6-128">O grupo de recursos do volume de destino de replicação da ANF</span><span class="sxs-lookup"><span data-stu-id="b5aa6-128">The resource group of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5aa6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5aa6-129">-ResourceId</span></span>
<span data-ttu-id="b5aa6-130">A ID do recurso do volume de destino de replicação da ANF</span><span class="sxs-lookup"><span data-stu-id="b5aa6-130">The resource id of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5aa6-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b5aa6-131">-Confirm</span></span>
<span data-ttu-id="b5aa6-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5aa6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5aa6-133">-WhatIf</span></span>
<span data-ttu-id="b5aa6-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5aa6-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5aa6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5aa6-136">CommonParameters</span></span>
<span data-ttu-id="b5aa6-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5aa6-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5aa6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5aa6-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="b5aa6-139">INPUTS</span></span>

### <span data-ttu-id="b5aa6-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b5aa6-140">System.String</span></span>

### <span data-ttu-id="b5aa6-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b5aa6-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="b5aa6-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="b5aa6-142">OUTPUTS</span></span>

### <span data-ttu-id="b5aa6-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b5aa6-143">System.Boolean</span></span>

## <span data-ttu-id="b5aa6-144">Notas</span><span class="sxs-lookup"><span data-stu-id="b5aa6-144">NOTES</span></span>

## <span data-ttu-id="b5aa6-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5aa6-145">RELATED LINKS</span></span>
