---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: e1ebab6e0b32c6358defee30512185868581b6e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112926"
---
# <span data-ttu-id="e6ecf-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="e6ecf-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="e6ecf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="e6ecf-103">Cria um novo pool de Arquivos Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="e6ecf-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="e6ecf-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6ecf-104">SYNTAX</span></span>

### <span data-ttu-id="e6ecf-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e6ecf-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6ecf-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6ecf-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6ecf-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6ecf-107">DESCRIPTION</span></span>
<span data-ttu-id="e6ecf-108">O **cmdlet New-AzNetAppFilesPool** cria um pool ANF.</span><span class="sxs-lookup"><span data-stu-id="e6ecf-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="e6ecf-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e6ecf-109">EXAMPLES</span></span>

### <span data-ttu-id="e6ecf-110">Exemplo 1: Criar um pool de ANF</span><span class="sxs-lookup"><span data-stu-id="e6ecf-110">Example 1: Create an ANF pool</span></span>
```
PS C:\>New-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool" -l "westus2" -PoolSize 4398046511104 -ServiceLevel "Premium" -QosType "Auto"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
TotalThroughputMibps: 262.144
UtilizedThroughputMibps: 164.221
QosType           : Auto
ProvisioningState : Succeeded
```

<span data-ttu-id="e6ecf-111">Esse comando cria o novo pool ANF "MyAnfPool" dentro da conta "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="e6ecf-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="e6ecf-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6ecf-112">PARAMETERS</span></span>

### <span data-ttu-id="e6ecf-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="e6ecf-113">-AccountName</span></span>
<span data-ttu-id="e6ecf-114">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="e6ecf-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="e6ecf-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="e6ecf-115">-AccountObject</span></span>
<span data-ttu-id="e6ecf-116">A conta do novo objeto de pool</span><span class="sxs-lookup"><span data-stu-id="e6ecf-116">The account for the new pool object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ecf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6ecf-117">-DefaultProfile</span></span>
<span data-ttu-id="e6ecf-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e6ecf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6ecf-119">-Local</span><span class="sxs-lookup"><span data-stu-id="e6ecf-119">-Location</span></span>
<span data-ttu-id="e6ecf-120">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="e6ecf-120">The location of the resource</span></span>

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

### <span data-ttu-id="e6ecf-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6ecf-121">-Name</span></span>
<span data-ttu-id="e6ecf-122">O nome do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="e6ecf-122">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ecf-123">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="e6ecf-123">-PoolSize</span></span>
<span data-ttu-id="e6ecf-124">O tamanho do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="e6ecf-124">The size of the ANF pool</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ecf-125">-QosType</span><span class="sxs-lookup"><span data-stu-id="e6ecf-125">-QosType</span></span>
<span data-ttu-id="e6ecf-126">O tipo de qos do pool.</span><span class="sxs-lookup"><span data-stu-id="e6ecf-126">The qos type of the pool.</span></span> <span data-ttu-id="e6ecf-127">Os valores possíveis incluem: 'Automático', 'Manual'</span><span class="sxs-lookup"><span data-stu-id="e6ecf-127">Possible values include: 'Auto', 'Manual'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Auto
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ecf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6ecf-128">-ResourceGroupName</span></span>
<span data-ttu-id="e6ecf-129">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="e6ecf-129">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="e6ecf-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="e6ecf-130">-ServiceLevel</span></span>
<span data-ttu-id="e6ecf-131">O nível de serviço do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="e6ecf-131">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="e6ecf-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="e6ecf-132">-Tag</span></span>
<span data-ttu-id="e6ecf-133">Uma tabela hash que representa marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="e6ecf-133">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ecf-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e6ecf-134">-Confirm</span></span>
<span data-ttu-id="e6ecf-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6ecf-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6ecf-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6ecf-136">-WhatIf</span></span>
<span data-ttu-id="e6ecf-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e6ecf-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6ecf-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e6ecf-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6ecf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6ecf-139">CommonParameters</span></span>
<span data-ttu-id="e6ecf-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6ecf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6ecf-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6ecf-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6ecf-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="e6ecf-142">INPUTS</span></span>

### <span data-ttu-id="e6ecf-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="e6ecf-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="e6ecf-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="e6ecf-144">OUTPUTS</span></span>

### <span data-ttu-id="e6ecf-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="e6ecf-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="e6ecf-146">Notas</span><span class="sxs-lookup"><span data-stu-id="e6ecf-146">NOTES</span></span>

## <span data-ttu-id="e6ecf-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6ecf-147">RELATED LINKS</span></span>
