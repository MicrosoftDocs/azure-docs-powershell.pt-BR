---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: c28b53fcd9b65198554f34cacd6f628d977e703a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947727"
---
# <span data-ttu-id="649ad-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="649ad-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="649ad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="649ad-102">SYNOPSIS</span></span>
<span data-ttu-id="649ad-103">Atualiza um volume de arquivos do Azure NetApp (ANF) de acordo com os modificadores opcionais fornecidos.</span><span class="sxs-lookup"><span data-stu-id="649ad-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="649ad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="649ad-104">SYNTAX</span></span>

### <span data-ttu-id="649ad-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="649ad-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="649ad-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="649ad-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="649ad-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="649ad-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="649ad-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="649ad-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="649ad-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="649ad-109">DESCRIPTION</span></span>
<span data-ttu-id="649ad-110">O cmdlet **Update-AzNetAppFilesVolume** atualiza um volume ANF.</span><span class="sxs-lookup"><span data-stu-id="649ad-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="649ad-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="649ad-111">EXAMPLES</span></span>

### <span data-ttu-id="649ad-112">Exemplo 1: atualizar um volume do ANF</span><span class="sxs-lookup"><span data-stu-id="649ad-112">Example 1: Update an ANF volume</span></span>
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

<span data-ttu-id="649ad-113">Esse comando atualiza o volume ANF "MyAnfVolume" com o novo tamanho UsageThreshold.</span><span class="sxs-lookup"><span data-stu-id="649ad-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="649ad-114">OS</span><span class="sxs-lookup"><span data-stu-id="649ad-114">PARAMETERS</span></span>

### <span data-ttu-id="649ad-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="649ad-115">-AccountName</span></span>
<span data-ttu-id="649ad-116">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="649ad-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="649ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="649ad-117">-DefaultProfile</span></span>
<span data-ttu-id="649ad-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="649ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="649ad-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="649ad-119">-ExportPolicy</span></span>
<span data-ttu-id="649ad-120">Uma matriz de Hashtable que representa a política de exportação</span><span class="sxs-lookup"><span data-stu-id="649ad-120">A hashtable array which represents the export policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeExportPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="649ad-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="649ad-121">-InputObject</span></span>
<span data-ttu-id="649ad-122">O objeto volume a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="649ad-122">The volume object to update</span></span>

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

### <span data-ttu-id="649ad-123">-Local</span><span class="sxs-lookup"><span data-stu-id="649ad-123">-Location</span></span>
<span data-ttu-id="649ad-124">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="649ad-124">The location of the resource</span></span>

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

### <span data-ttu-id="649ad-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="649ad-125">-Name</span></span>
<span data-ttu-id="649ad-126">O nome do volume ANF</span><span class="sxs-lookup"><span data-stu-id="649ad-126">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="649ad-127">-PoolName</span><span class="sxs-lookup"><span data-stu-id="649ad-127">-PoolName</span></span>
<span data-ttu-id="649ad-128">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="649ad-128">The name of the ANF pool</span></span>

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

### <span data-ttu-id="649ad-129">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="649ad-129">-PoolObject</span></span>
<span data-ttu-id="649ad-130">O objeto de pool que contém o volume a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="649ad-130">The pool object containing the volume to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="649ad-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="649ad-131">-ResourceGroupName</span></span>
<span data-ttu-id="649ad-132">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="649ad-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="649ad-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="649ad-133">-ResourceId</span></span>
<span data-ttu-id="649ad-134">A ID do recurso do volume ANF</span><span class="sxs-lookup"><span data-stu-id="649ad-134">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="649ad-135">-Nível de</span><span class="sxs-lookup"><span data-stu-id="649ad-135">-ServiceLevel</span></span>
<span data-ttu-id="649ad-136">O nível de serviço do volume ANF</span><span class="sxs-lookup"><span data-stu-id="649ad-136">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="649ad-137">-Marca</span><span class="sxs-lookup"><span data-stu-id="649ad-137">-Tag</span></span>
<span data-ttu-id="649ad-138">Uma Hashtable que representa as marcas de recursos</span><span class="sxs-lookup"><span data-stu-id="649ad-138">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="649ad-139">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="649ad-139">-UsageThreshold</span></span>
<span data-ttu-id="649ad-140">A cota máxima de armazenamento permitida para um sistema de arquivos em bytes</span><span class="sxs-lookup"><span data-stu-id="649ad-140">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="649ad-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="649ad-141">-Confirm</span></span>
<span data-ttu-id="649ad-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="649ad-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="649ad-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="649ad-143">-WhatIf</span></span>
<span data-ttu-id="649ad-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="649ad-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="649ad-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="649ad-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="649ad-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="649ad-146">CommonParameters</span></span>
<span data-ttu-id="649ad-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="649ad-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="649ad-148">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="649ad-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="649ad-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="649ad-149">INPUTS</span></span>

### <span data-ttu-id="649ad-150">System. String</span><span class="sxs-lookup"><span data-stu-id="649ad-150">System.String</span></span>

### <span data-ttu-id="649ad-151">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="649ad-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="649ad-152">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="649ad-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="649ad-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="649ad-153">OUTPUTS</span></span>

### <span data-ttu-id="649ad-154">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="649ad-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="649ad-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="649ad-155">NOTES</span></span>

## <span data-ttu-id="649ad-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="649ad-156">RELATED LINKS</span></span>
