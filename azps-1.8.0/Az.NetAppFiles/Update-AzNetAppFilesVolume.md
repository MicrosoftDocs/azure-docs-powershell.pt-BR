---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: ea943c490a87dd4c62752b97753971f0941ed3b9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600758"
---
# <span data-ttu-id="6d6a6-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="6d6a6-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="6d6a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d6a6-102">SYNOPSIS</span></span>
<span data-ttu-id="6d6a6-103">Atualiza um volume de arquivos do Azure NetApp (ANF) de acordo com os modificadores opcionais fornecidos.</span><span class="sxs-lookup"><span data-stu-id="6d6a6-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="6d6a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d6a6-104">SYNTAX</span></span>

### <span data-ttu-id="6d6a6-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6d6a6-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d6a6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d6a6-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d6a6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d6a6-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d6a6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d6a6-108">DESCRIPTION</span></span>
<span data-ttu-id="6d6a6-109">O cmdlet **Update-AzNetAppFilesVolume** atualiza um volume ANF.</span><span class="sxs-lookup"><span data-stu-id="6d6a6-109">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="6d6a6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d6a6-110">EXAMPLES</span></span>

### <span data-ttu-id="6d6a6-111">Exemplo 1: atualizar um volume do ANF</span><span class="sxs-lookup"><span data-stu-id="6d6a6-111">Example 1: Update an ANF volume</span></span>
```
PS C:\>Update-AzNetAppFilesVolume -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -UsageThreshold Size

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 2199023255552
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="6d6a6-112">Esse comando atualiza o volume ANF "MyAnfVolume" com o novo tamanho UsageThreshold.</span><span class="sxs-lookup"><span data-stu-id="6d6a6-112">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="6d6a6-113">OS</span><span class="sxs-lookup"><span data-stu-id="6d6a6-113">PARAMETERS</span></span>

### <span data-ttu-id="6d6a6-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6d6a6-114">-AccountName</span></span>
<span data-ttu-id="6d6a6-115">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="6d6a6-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="6d6a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d6a6-116">-DefaultProfile</span></span>
<span data-ttu-id="6d6a6-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d6a6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d6a6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d6a6-118">-InputObject</span></span>
<span data-ttu-id="6d6a6-119">O objeto volume a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="6d6a6-119">The volume object to update</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d6a6-120">-Local</span><span class="sxs-lookup"><span data-stu-id="6d6a6-120">-Location</span></span>
<span data-ttu-id="6d6a6-121">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="6d6a6-121">The location of the resource</span></span>

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

### <span data-ttu-id="6d6a6-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d6a6-122">-Name</span></span>
<span data-ttu-id="6d6a6-123">O nome do volume ANF</span><span class="sxs-lookup"><span data-stu-id="6d6a6-123">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d6a6-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="6d6a6-124">-PoolName</span></span>
<span data-ttu-id="6d6a6-125">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="6d6a6-125">The name of the ANF pool</span></span>

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

### <span data-ttu-id="6d6a6-126">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="6d6a6-126">-PoolObject</span></span>
<span data-ttu-id="6d6a6-127">O objeto de pool que contém o volume a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="6d6a6-127">The pool object containing the volume to update</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d6a6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d6a6-128">-ResourceGroupName</span></span>
<span data-ttu-id="6d6a6-129">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="6d6a6-129">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="6d6a6-130">-Nível de</span><span class="sxs-lookup"><span data-stu-id="6d6a6-130">-ServiceLevel</span></span>
<span data-ttu-id="6d6a6-131">O nível de serviço do volume ANF</span><span class="sxs-lookup"><span data-stu-id="6d6a6-131">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="6d6a6-132">-Marca</span><span class="sxs-lookup"><span data-stu-id="6d6a6-132">-Tag</span></span>
<span data-ttu-id="6d6a6-133">Uma Hashtable que representa as marcas de recursos</span><span class="sxs-lookup"><span data-stu-id="6d6a6-133">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="6d6a6-134">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="6d6a6-134">-UsageThreshold</span></span>
<span data-ttu-id="6d6a6-135">A cota máxima de armazenamento permitida para um sistema de arquivos em bytes</span><span class="sxs-lookup"><span data-stu-id="6d6a6-135">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="6d6a6-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6d6a6-136">-Confirm</span></span>
<span data-ttu-id="6d6a6-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d6a6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d6a6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d6a6-138">-WhatIf</span></span>
<span data-ttu-id="6d6a6-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6d6a6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d6a6-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6d6a6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d6a6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d6a6-141">CommonParameters</span></span>
<span data-ttu-id="6d6a6-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d6a6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6d6a6-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d6a6-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d6a6-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d6a6-144">INPUTS</span></span>

### <span data-ttu-id="6d6a6-145">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="6d6a6-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="6d6a6-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="6d6a6-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="6d6a6-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d6a6-147">OUTPUTS</span></span>

### <span data-ttu-id="6d6a6-148">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="6d6a6-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="6d6a6-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d6a6-149">NOTES</span></span>

## <span data-ttu-id="6d6a6-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d6a6-150">RELATED LINKS</span></span>
