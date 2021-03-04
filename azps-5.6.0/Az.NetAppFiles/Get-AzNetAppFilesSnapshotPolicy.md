---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: 3e93792a8698999599f67be84c3fe01e9c2ae508
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887458"
---
# <span data-ttu-id="e33a4-101">Get-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="e33a4-101">Get-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="e33a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e33a4-102">SYNOPSIS</span></span>
<span data-ttu-id="e33a4-103">Obtém detalhes de uma política de instantâneo do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="e33a4-103">Gets details of an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="e33a4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e33a4-104">SYNTAX</span></span>

### <span data-ttu-id="e33a4-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e33a4-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e33a4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e33a4-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e33a4-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e33a4-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e33a4-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e33a4-108">DESCRIPTION</span></span>
<span data-ttu-id="e33a4-109">O cmdlet **Get-AzNetAppFilesSnapshotPolicy** obtém detalhes de uma política de instantâneo ANF.</span><span class="sxs-lookup"><span data-stu-id="e33a4-109">The **Get-AzNetAppFilesSnapshotPolicy** cmdlet gets details of an ANF snapshot policy.</span></span>

## <span data-ttu-id="e33a4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e33a4-110">EXAMPLES</span></span>

### <span data-ttu-id="e33a4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e33a4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="e33a4-112">Este comando obtém a política de backup chamada "MyBackupPolicy" para a conta "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="e33a4-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="e33a4-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e33a4-113">PARAMETERS</span></span>

### <span data-ttu-id="e33a4-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e33a4-114">-AccountName</span></span>
<span data-ttu-id="e33a4-115">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="e33a4-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="e33a4-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="e33a4-116">-AccountObject</span></span>
<span data-ttu-id="e33a4-117">A conta do novo objeto De política de instantâneo</span><span class="sxs-lookup"><span data-stu-id="e33a4-117">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="e33a4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e33a4-118">-DefaultProfile</span></span>
<span data-ttu-id="e33a4-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e33a4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e33a4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e33a4-120">-Name</span></span>
<span data-ttu-id="e33a4-121">O nome da política de instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="e33a4-121">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotPolicyName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e33a4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e33a4-122">-ResourceGroupName</span></span>
<span data-ttu-id="e33a4-123">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="e33a4-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="e33a4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e33a4-124">-ResourceId</span></span>
<span data-ttu-id="e33a4-125">A id de recurso da Política de Instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="e33a4-125">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="e33a4-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e33a4-126">-Confirm</span></span>
<span data-ttu-id="e33a4-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e33a4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e33a4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e33a4-128">-WhatIf</span></span>
<span data-ttu-id="e33a4-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e33a4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e33a4-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e33a4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e33a4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e33a4-131">CommonParameters</span></span>
<span data-ttu-id="e33a4-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e33a4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e33a4-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e33a4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e33a4-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e33a4-134">INPUTS</span></span>

### <span data-ttu-id="e33a4-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e33a4-135">System.String</span></span>

### <span data-ttu-id="e33a4-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="e33a4-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="e33a4-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e33a4-137">OUTPUTS</span></span>

### <span data-ttu-id="e33a4-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="e33a4-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="e33a4-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="e33a4-139">NOTES</span></span>

## <span data-ttu-id="e33a4-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e33a4-140">RELATED LINKS</span></span>
