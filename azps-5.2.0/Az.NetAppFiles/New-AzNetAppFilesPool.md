---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: e1ebab6e0b32c6358defee30512185868581b6e7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262614"
---
# <span data-ttu-id="ffa86-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="ffa86-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="ffa86-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ffa86-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa86-103">Cria um novo pool de arquivos do Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="ffa86-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="ffa86-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ffa86-104">SYNTAX</span></span>

### <span data-ttu-id="ffa86-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ffa86-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffa86-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffa86-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffa86-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ffa86-107">DESCRIPTION</span></span>
<span data-ttu-id="ffa86-108">O cmdlet **New-AzNetAppFilesPool** cria um pool ANF.</span><span class="sxs-lookup"><span data-stu-id="ffa86-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="ffa86-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ffa86-109">EXAMPLES</span></span>

### <span data-ttu-id="ffa86-110">Exemplo 1: criar um pool de ANF</span><span class="sxs-lookup"><span data-stu-id="ffa86-110">Example 1: Create an ANF pool</span></span>
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

<span data-ttu-id="ffa86-111">Esse comando cria o novo pool de ANF "MyAnfPool" na conta "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="ffa86-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="ffa86-112">OS</span><span class="sxs-lookup"><span data-stu-id="ffa86-112">PARAMETERS</span></span>

### <span data-ttu-id="ffa86-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ffa86-113">-AccountName</span></span>
<span data-ttu-id="ffa86-114">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="ffa86-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="ffa86-115">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="ffa86-115">-AccountObject</span></span>
<span data-ttu-id="ffa86-116">A conta para o novo objeto de pool</span><span class="sxs-lookup"><span data-stu-id="ffa86-116">The account for the new pool object</span></span>

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

### <span data-ttu-id="ffa86-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffa86-117">-DefaultProfile</span></span>
<span data-ttu-id="ffa86-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ffa86-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffa86-119">-Local</span><span class="sxs-lookup"><span data-stu-id="ffa86-119">-Location</span></span>
<span data-ttu-id="ffa86-120">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="ffa86-120">The location of the resource</span></span>

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

### <span data-ttu-id="ffa86-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ffa86-121">-Name</span></span>
<span data-ttu-id="ffa86-122">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="ffa86-122">The name of the ANF pool</span></span>

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

### <span data-ttu-id="ffa86-123">-Agrupamento</span><span class="sxs-lookup"><span data-stu-id="ffa86-123">-PoolSize</span></span>
<span data-ttu-id="ffa86-124">O tamanho do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="ffa86-124">The size of the ANF pool</span></span>

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

### <span data-ttu-id="ffa86-125">-QosType</span><span class="sxs-lookup"><span data-stu-id="ffa86-125">-QosType</span></span>
<span data-ttu-id="ffa86-126">O tipo de QoS do pool.</span><span class="sxs-lookup"><span data-stu-id="ffa86-126">The qos type of the pool.</span></span> <span data-ttu-id="ffa86-127">Os valores possíveis incluem: ' auto ', ' manual '</span><span class="sxs-lookup"><span data-stu-id="ffa86-127">Possible values include: 'Auto', 'Manual'</span></span>

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

### <span data-ttu-id="ffa86-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffa86-128">-ResourceGroupName</span></span>
<span data-ttu-id="ffa86-129">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="ffa86-129">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="ffa86-130">-Nível de</span><span class="sxs-lookup"><span data-stu-id="ffa86-130">-ServiceLevel</span></span>
<span data-ttu-id="ffa86-131">O nível de serviço do pool ANF</span><span class="sxs-lookup"><span data-stu-id="ffa86-131">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="ffa86-132">-Marca</span><span class="sxs-lookup"><span data-stu-id="ffa86-132">-Tag</span></span>
<span data-ttu-id="ffa86-133">Uma Hashtable que representa as marcas de recursos</span><span class="sxs-lookup"><span data-stu-id="ffa86-133">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="ffa86-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ffa86-134">-Confirm</span></span>
<span data-ttu-id="ffa86-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffa86-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffa86-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffa86-136">-WhatIf</span></span>
<span data-ttu-id="ffa86-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ffa86-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffa86-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ffa86-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffa86-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa86-139">CommonParameters</span></span>
<span data-ttu-id="ffa86-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffa86-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa86-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ffa86-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa86-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ffa86-142">INPUTS</span></span>

### <span data-ttu-id="ffa86-143">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="ffa86-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="ffa86-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ffa86-144">OUTPUTS</span></span>

### <span data-ttu-id="ffa86-145">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="ffa86-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="ffa86-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ffa86-146">NOTES</span></span>

## <span data-ttu-id="ffa86-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ffa86-147">RELATED LINKS</span></span>
