---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: f7dc2473818b1e80503a4583993d818818c9aec0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772128"
---
# <span data-ttu-id="fcb43-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="fcb43-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="fcb43-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fcb43-102">SYNOPSIS</span></span>
<span data-ttu-id="fcb43-103">Atualiza um pool de arquivos do Azure NetApp (ANF) de acordo com os modificadores opcionais fornecidos.</span><span class="sxs-lookup"><span data-stu-id="fcb43-103">Updates an Azure NetApp Files (ANF) pool according to the optional modifiers provided.</span></span>

## <span data-ttu-id="fcb43-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fcb43-104">SYNTAX</span></span>

### <span data-ttu-id="fcb43-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fcb43-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> [-Location <String>] -AccountName <String> -Name <String>
 [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcb43-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcb43-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcb43-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcb43-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcb43-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcb43-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fcb43-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fcb43-109">DESCRIPTION</span></span>
<span data-ttu-id="fcb43-110">O cmdlet **Update-AzNetAppFilesPool** modifica um pool de ANF.</span><span class="sxs-lookup"><span data-stu-id="fcb43-110">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="fcb43-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fcb43-111">EXAMPLES</span></span>

### <span data-ttu-id="fcb43-112">Exemplo 1: modificar um pool de ANF</span><span class="sxs-lookup"><span data-stu-id="fcb43-112">Example 1: Modify an ANF pool</span></span>
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

<span data-ttu-id="fcb43-113">Esse comando altera o pool de ANF "MyAnfPool" para ter o tamanho e o nível de um determinado.</span><span class="sxs-lookup"><span data-stu-id="fcb43-113">This command changes the ANF pool "MyAnfPool" to have the given size and ServiceLevel.</span></span>

## <span data-ttu-id="fcb43-114">OS</span><span class="sxs-lookup"><span data-stu-id="fcb43-114">PARAMETERS</span></span>

### <span data-ttu-id="fcb43-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fcb43-115">-AccountName</span></span>
<span data-ttu-id="fcb43-116">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="fcb43-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="fcb43-117">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="fcb43-117">-AccountObject</span></span>
<span data-ttu-id="fcb43-118">O objeto de conta que contém o pool a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="fcb43-118">The account object containing the pool to update</span></span>

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

### <span data-ttu-id="fcb43-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcb43-119">-DefaultProfile</span></span>
<span data-ttu-id="fcb43-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fcb43-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcb43-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcb43-121">-InputObject</span></span>
<span data-ttu-id="fcb43-122">O objeto de pool a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="fcb43-122">The pool object to update</span></span>

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

### <span data-ttu-id="fcb43-123">-Local</span><span class="sxs-lookup"><span data-stu-id="fcb43-123">-Location</span></span>
<span data-ttu-id="fcb43-124">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="fcb43-124">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcb43-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="fcb43-125">-Name</span></span>
<span data-ttu-id="fcb43-126">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="fcb43-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="fcb43-127">-Agrupamento</span><span class="sxs-lookup"><span data-stu-id="fcb43-127">-PoolSize</span></span>
<span data-ttu-id="fcb43-128">O tamanho do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="fcb43-128">The size of the ANF pool</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcb43-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcb43-129">-ResourceGroupName</span></span>
<span data-ttu-id="fcb43-130">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="fcb43-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="fcb43-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fcb43-131">-ResourceId</span></span>
<span data-ttu-id="fcb43-132">A ID do recurso do pool ANF</span><span class="sxs-lookup"><span data-stu-id="fcb43-132">The resource id of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcb43-133">-Nível de</span><span class="sxs-lookup"><span data-stu-id="fcb43-133">-ServiceLevel</span></span>
<span data-ttu-id="fcb43-134">O nível de serviço do pool ANF</span><span class="sxs-lookup"><span data-stu-id="fcb43-134">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="fcb43-135">-Marca</span><span class="sxs-lookup"><span data-stu-id="fcb43-135">-Tag</span></span>
<span data-ttu-id="fcb43-136">Uma Hashtable que representa as marcas de recursos</span><span class="sxs-lookup"><span data-stu-id="fcb43-136">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcb43-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fcb43-137">-Confirm</span></span>
<span data-ttu-id="fcb43-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcb43-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcb43-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcb43-139">-WhatIf</span></span>
<span data-ttu-id="fcb43-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fcb43-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcb43-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fcb43-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcb43-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcb43-142">CommonParameters</span></span>
<span data-ttu-id="fcb43-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcb43-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fcb43-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcb43-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcb43-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fcb43-145">INPUTS</span></span>

### <span data-ttu-id="fcb43-146">System. String</span><span class="sxs-lookup"><span data-stu-id="fcb43-146">System.String</span></span>

### <span data-ttu-id="fcb43-147">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="fcb43-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="fcb43-148">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="fcb43-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="fcb43-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fcb43-149">OUTPUTS</span></span>

### <span data-ttu-id="fcb43-150">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="fcb43-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="fcb43-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fcb43-151">NOTES</span></span>

## <span data-ttu-id="fcb43-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fcb43-152">RELATED LINKS</span></span>
