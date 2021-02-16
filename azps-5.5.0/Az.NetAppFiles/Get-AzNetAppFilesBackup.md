---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
ms.openlocfilehash: 46f6f5d7f9d843a9dd6d30053e9205e52be989d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113539"
---
# <span data-ttu-id="de130-101">Get-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="de130-101">Get-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="de130-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de130-102">SYNOPSIS</span></span>
<span data-ttu-id="de130-103">Obtém detalhes de um backup do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="de130-103">Gets details of an Azure NetApp Files (ANF) Backup.</span></span>

## <span data-ttu-id="de130-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de130-104">SYNTAX</span></span>

### <span data-ttu-id="de130-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="de130-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackup -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 [-VolumeName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de130-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de130-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="de130-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de130-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de130-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="de130-108">DESCRIPTION</span></span>
<span data-ttu-id="de130-109">O cmdlet **Get-AzNetAppFilesBackup** obtém detalhes de um backup ANF.</span><span class="sxs-lookup"><span data-stu-id="de130-109">The **Get-AzNetAppFilesBackup** cmdlet gets details of an ANF backup.</span></span>

## <span data-ttu-id="de130-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="de130-110">EXAMPLES</span></span>

### <span data-ttu-id="de130-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="de130-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="de130-112">Esse comando obtém o backcup chamado "MyAnfAccount" do volume chamado "MyVolume".</span><span class="sxs-lookup"><span data-stu-id="de130-112">This command gets the backcup named "MyAnfAccount" from the volume named "MyVolume".</span></span>

## <span data-ttu-id="de130-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de130-113">PARAMETERS</span></span>

### <span data-ttu-id="de130-114">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="de130-114">-AccountName</span></span>
<span data-ttu-id="de130-115">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="de130-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="de130-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de130-116">-DefaultProfile</span></span>
<span data-ttu-id="de130-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de130-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de130-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="de130-118">-Name</span></span>
<span data-ttu-id="de130-119">O nome do backup da ANF</span><span class="sxs-lookup"><span data-stu-id="de130-119">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de130-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="de130-120">-PoolName</span></span>
<span data-ttu-id="de130-121">O nome do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="de130-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="de130-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de130-122">-ResourceGroupName</span></span>
<span data-ttu-id="de130-123">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="de130-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="de130-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de130-124">-ResourceId</span></span>
<span data-ttu-id="de130-125">A ID do recurso do Backup ANF</span><span class="sxs-lookup"><span data-stu-id="de130-125">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="de130-126">-Nomedo Volume</span><span class="sxs-lookup"><span data-stu-id="de130-126">-VolumeName</span></span>
<span data-ttu-id="de130-127">O nome do volume da ANF</span><span class="sxs-lookup"><span data-stu-id="de130-127">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de130-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="de130-128">-VolumeObject</span></span>
<span data-ttu-id="de130-129">O objeto de volume que contém o backup a ser retornado</span><span class="sxs-lookup"><span data-stu-id="de130-129">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="de130-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de130-130">CommonParameters</span></span>
<span data-ttu-id="de130-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de130-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de130-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de130-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de130-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="de130-133">INPUTS</span></span>

### <span data-ttu-id="de130-134">System.String</span><span class="sxs-lookup"><span data-stu-id="de130-134">System.String</span></span>

### <span data-ttu-id="de130-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="de130-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="de130-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="de130-136">OUTPUTS</span></span>

### <span data-ttu-id="de130-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="de130-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="de130-138">Notas</span><span class="sxs-lookup"><span data-stu-id="de130-138">NOTES</span></span>

## <span data-ttu-id="de130-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de130-139">RELATED LINKS</span></span>
