---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: 3dd02a2dc0cf7090ba2711b6155d25038397ab9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600759"
---
# <span data-ttu-id="3294d-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="3294d-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="3294d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3294d-102">SYNOPSIS</span></span>
<span data-ttu-id="3294d-103">Atualiza um pool de arquivos do Azure NetApp (ANF) com o novo conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="3294d-103">Updates an Azure NetApp Files (ANF) pool with the new data set.</span></span>

## <span data-ttu-id="3294d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3294d-104">SYNTAX</span></span>

### <span data-ttu-id="3294d-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3294d-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3294d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3294d-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String>
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3294d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3294d-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -PoolSize <Int64> -ServiceLevel <String> -InputObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3294d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3294d-108">DESCRIPTION</span></span>
<span data-ttu-id="3294d-109">O cmdlet **Update-AzNetAppFilesPool** modifica um pool de ANF.</span><span class="sxs-lookup"><span data-stu-id="3294d-109">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="3294d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3294d-110">EXAMPLES</span></span>

### <span data-ttu-id="3294d-111">Exemplo 1: modificar um pool de ANF</span><span class="sxs-lookup"><span data-stu-id="3294d-111">Example 1: Modify an ANF pool</span></span>
```
PS C:\>Update-AzNetAppFilesPool -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolSize 4398046511104 -ServiceLevel "Standard"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
Size              : 4398046511104
ServiceLevel      : Standard
ProvisioningState : Succeeded
```

<span data-ttu-id="3294d-112">Esse comando altera o pool de ANF "MyAnfPool" para ter o tamanho e o nível de um determinado.</span><span class="sxs-lookup"><span data-stu-id="3294d-112">This command changes the ANF pool "MyAnfPool" to have the given size and ServiceLevel.</span></span>

## <span data-ttu-id="3294d-113">OS</span><span class="sxs-lookup"><span data-stu-id="3294d-113">PARAMETERS</span></span>

### <span data-ttu-id="3294d-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3294d-114">-AccountName</span></span>
<span data-ttu-id="3294d-115">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="3294d-115">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3294d-116">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="3294d-116">-AccountObject</span></span>
<span data-ttu-id="3294d-117">O objeto de conta que contém o pool a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="3294d-117">The account object containing the pool to update</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3294d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3294d-118">-DefaultProfile</span></span>
<span data-ttu-id="3294d-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3294d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3294d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3294d-120">-InputObject</span></span>
<span data-ttu-id="3294d-121">O objeto de pool a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="3294d-121">The pool object to update</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3294d-122">-Local</span><span class="sxs-lookup"><span data-stu-id="3294d-122">-Location</span></span>
<span data-ttu-id="3294d-123">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="3294d-123">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3294d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="3294d-124">-Name</span></span>
<span data-ttu-id="3294d-125">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="3294d-125">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3294d-126">-Agrupamento</span><span class="sxs-lookup"><span data-stu-id="3294d-126">-PoolSize</span></span>
<span data-ttu-id="3294d-127">O tamanho do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="3294d-127">The size of the ANF pool</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3294d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3294d-128">-ResourceGroupName</span></span>
<span data-ttu-id="3294d-129">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="3294d-129">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3294d-130">-Nível de</span><span class="sxs-lookup"><span data-stu-id="3294d-130">-ServiceLevel</span></span>
<span data-ttu-id="3294d-131">O nível de serviço do pool ANF</span><span class="sxs-lookup"><span data-stu-id="3294d-131">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="3294d-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3294d-132">-Confirm</span></span>
<span data-ttu-id="3294d-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3294d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3294d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3294d-134">-WhatIf</span></span>
<span data-ttu-id="3294d-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3294d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3294d-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3294d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3294d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3294d-137">CommonParameters</span></span>
<span data-ttu-id="3294d-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3294d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3294d-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3294d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3294d-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3294d-140">INPUTS</span></span>

### <span data-ttu-id="3294d-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="3294d-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="3294d-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="3294d-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="3294d-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3294d-143">OUTPUTS</span></span>

### <span data-ttu-id="3294d-144">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="3294d-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="3294d-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3294d-145">NOTES</span></span>

## <span data-ttu-id="3294d-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3294d-146">RELATED LINKS</span></span>
