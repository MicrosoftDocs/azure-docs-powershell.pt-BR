---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
ms.openlocfilehash: 66ba63b3e350093173ae9d1badc6c717a3c682aa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427053"
---
# <span data-ttu-id="f6518-101">New-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="f6518-101">New-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="f6518-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6518-102">SYNOPSIS</span></span>
<span data-ttu-id="f6518-103">Cria um novo backup do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="f6518-103">Creates a new Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="f6518-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6518-104">SYNTAX</span></span>

### <span data-ttu-id="f6518-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f6518-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> -Label <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6518-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6518-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackup -Name <String> -Label <String> -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6518-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f6518-107">DESCRIPTION</span></span>
<span data-ttu-id="f6518-108">O cmdlet **New-AzNetAppFilesBackup** cria um backup para um volume ANF.</span><span class="sxs-lookup"><span data-stu-id="f6518-108">The **New-AzNetAppFilesBackup** cmdlet creates a backup for an ANF volume.</span></span>

## <span data-ttu-id="f6518-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6518-109">EXAMPLES</span></span>

### <span data-ttu-id="f6518-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f6518-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackup -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyVolumeBackup" -Label "ALabel"
```

<span data-ttu-id="f6518-111">Esse comando cria o novo ANF backup para o volume chamado "myvolume".</span><span class="sxs-lookup"><span data-stu-id="f6518-111">This command creates the new ANF backup for volume named  account "MyVolume".</span></span>

## <span data-ttu-id="f6518-112">OS</span><span class="sxs-lookup"><span data-stu-id="f6518-112">PARAMETERS</span></span>

### <span data-ttu-id="f6518-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f6518-113">-AccountName</span></span>
<span data-ttu-id="f6518-114">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="f6518-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="f6518-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6518-115">-DefaultProfile</span></span>
<span data-ttu-id="f6518-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6518-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6518-117">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="f6518-117">-Label</span></span>
<span data-ttu-id="f6518-118">Rótulo para backup</span><span class="sxs-lookup"><span data-stu-id="f6518-118">Label for backup</span></span>

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

### <span data-ttu-id="f6518-119">-Local</span><span class="sxs-lookup"><span data-stu-id="f6518-119">-Location</span></span>
<span data-ttu-id="f6518-120">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="f6518-120">The location of the resource</span></span>

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

### <span data-ttu-id="f6518-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6518-121">-Name</span></span>
<span data-ttu-id="f6518-122">O nome do backup do ANF</span><span class="sxs-lookup"><span data-stu-id="f6518-122">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6518-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="f6518-123">-PoolName</span></span>
<span data-ttu-id="f6518-124">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="f6518-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="f6518-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6518-125">-ResourceGroupName</span></span>
<span data-ttu-id="f6518-126">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="f6518-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="f6518-127">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="f6518-127">-VolumeName</span></span>
<span data-ttu-id="f6518-128">O nome do volume ANF</span><span class="sxs-lookup"><span data-stu-id="f6518-128">The name of the ANF volume</span></span>

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

### <span data-ttu-id="f6518-129">-Volumeobject</span><span class="sxs-lookup"><span data-stu-id="f6518-129">-VolumeObject</span></span>
<span data-ttu-id="f6518-130">O volume do novo objeto de backup</span><span class="sxs-lookup"><span data-stu-id="f6518-130">The volume for the new backup object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6518-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f6518-131">-Confirm</span></span>
<span data-ttu-id="f6518-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6518-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6518-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6518-133">-WhatIf</span></span>
<span data-ttu-id="f6518-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f6518-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6518-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f6518-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6518-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6518-136">CommonParameters</span></span>
<span data-ttu-id="f6518-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6518-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6518-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6518-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6518-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f6518-139">INPUTS</span></span>

### <span data-ttu-id="f6518-140">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f6518-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="f6518-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f6518-141">OUTPUTS</span></span>

### <span data-ttu-id="f6518-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="f6518-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="f6518-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f6518-143">NOTES</span></span>

## <span data-ttu-id="f6518-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6518-144">RELATED LINKS</span></span>
