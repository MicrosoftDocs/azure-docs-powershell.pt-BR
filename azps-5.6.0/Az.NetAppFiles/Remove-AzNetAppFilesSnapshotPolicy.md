---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: 06bdb5246cc0830ef78baa81d418f1fe6e51e935
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887422"
---
# <span data-ttu-id="b22df-101">Remove-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="b22df-101">Remove-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="b22df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b22df-102">SYNOPSIS</span></span>
<span data-ttu-id="b22df-103">Exclui uma política de instantâneo do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="b22df-103">Deletes an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="b22df-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b22df-104">SYNTAX</span></span>

### <span data-ttu-id="b22df-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b22df-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b22df-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b22df-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b22df-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b22df-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b22df-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b22df-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -InputObject <PSNetAppFilesSnapshotPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b22df-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b22df-109">DESCRIPTION</span></span>
<span data-ttu-id="b22df-110">O cmdlet **Remove-AzNetAppFilesSnapshotPolicy** exclui uma política de instantâneo ANF.</span><span class="sxs-lookup"><span data-stu-id="b22df-110">The **Remove-AzNetAppFilesSnapshotPolicy** cmdlet deletes an ANF snapshot policy.</span></span>

## <span data-ttu-id="b22df-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b22df-111">EXAMPLES</span></span>

### <span data-ttu-id="b22df-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b22df-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="b22df-113">Este comando exclui a nova política de backup ANF com o nome "MyBackupPolicy" para a conta "MyAccount".</span><span class="sxs-lookup"><span data-stu-id="b22df-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="b22df-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b22df-114">PARAMETERS</span></span>

### <span data-ttu-id="b22df-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b22df-115">-AccountName</span></span>
<span data-ttu-id="b22df-116">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="b22df-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="b22df-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="b22df-117">-AccountObject</span></span>
<span data-ttu-id="b22df-118">A conta do novo objeto De política de instantâneo</span><span class="sxs-lookup"><span data-stu-id="b22df-118">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="b22df-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b22df-119">-DefaultProfile</span></span>
<span data-ttu-id="b22df-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b22df-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b22df-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b22df-121">-InputObject</span></span>
<span data-ttu-id="b22df-122">O objeto SnapshotPolicy a ser removido</span><span class="sxs-lookup"><span data-stu-id="b22df-122">The SnapshotPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b22df-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b22df-123">-Name</span></span>
<span data-ttu-id="b22df-124">O nome da política de instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="b22df-124">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22df-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b22df-125">-PassThru</span></span>
<span data-ttu-id="b22df-126">Retornar se a conta especificada foi removida com êxito</span><span class="sxs-lookup"><span data-stu-id="b22df-126">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="b22df-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b22df-127">-ResourceGroupName</span></span>
<span data-ttu-id="b22df-128">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="b22df-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="b22df-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b22df-129">-ResourceId</span></span>
<span data-ttu-id="b22df-130">A id de recurso da Política de Instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="b22df-130">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="b22df-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b22df-131">-Confirm</span></span>
<span data-ttu-id="b22df-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b22df-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b22df-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b22df-133">-WhatIf</span></span>
<span data-ttu-id="b22df-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b22df-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b22df-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b22df-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b22df-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b22df-136">CommonParameters</span></span>
<span data-ttu-id="b22df-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b22df-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b22df-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b22df-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b22df-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b22df-139">INPUTS</span></span>

### <span data-ttu-id="b22df-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b22df-140">System.String</span></span>

### <span data-ttu-id="b22df-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="b22df-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="b22df-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="b22df-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="b22df-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b22df-143">OUTPUTS</span></span>

### <span data-ttu-id="b22df-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="b22df-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="b22df-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="b22df-145">NOTES</span></span>

## <span data-ttu-id="b22df-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b22df-146">RELATED LINKS</span></span>
