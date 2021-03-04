---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: de9d0cf5d989cfa4d910f8e5ee9d959393c42632
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887427"
---
# <span data-ttu-id="7a892-101">Remove-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="7a892-101">Remove-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="7a892-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a892-102">SYNOPSIS</span></span>
<span data-ttu-id="7a892-103">Exclui uma política de backup arquivos do Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="7a892-103">Deletes an Azure NetApp Files (ANF) backup policy.</span></span>

## <span data-ttu-id="7a892-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7a892-104">SYNTAX</span></span>

### <span data-ttu-id="7a892-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7a892-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a892-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a892-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a892-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a892-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a892-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a892-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -InputObject <PSNetAppFilesBackupPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a892-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7a892-109">DESCRIPTION</span></span>
<span data-ttu-id="7a892-110">O cmdlet **Remove-AzNetAppFilesBackupPolicy** exclui uma política de backup ANF.</span><span class="sxs-lookup"><span data-stu-id="7a892-110">The **Remove-AzNetAppFilesBackupPolicy** cmdlet deletes an ANF backup policy.</span></span>

## <span data-ttu-id="7a892-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a892-111">EXAMPLES</span></span>

### <span data-ttu-id="7a892-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7a892-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="7a892-113">Este comando exclui a nova política de backup ANF com o nome "MyBackupPolicy" para a conta "MyAccount".</span><span class="sxs-lookup"><span data-stu-id="7a892-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="7a892-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7a892-114">PARAMETERS</span></span>

### <span data-ttu-id="7a892-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7a892-115">-AccountName</span></span>
<span data-ttu-id="7a892-116">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="7a892-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="7a892-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="7a892-117">-AccountObject</span></span>
<span data-ttu-id="7a892-118">O objeto Account que contém a Política de Backup a ser removido</span><span class="sxs-lookup"><span data-stu-id="7a892-118">The Account object containing the Backup Policy to remove</span></span>

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

### <span data-ttu-id="7a892-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a892-119">-DefaultProfile</span></span>
<span data-ttu-id="7a892-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a892-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a892-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a892-121">-InputObject</span></span>
<span data-ttu-id="7a892-122">O objeto BackupPolicy a ser removido</span><span class="sxs-lookup"><span data-stu-id="7a892-122">The BackupPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a892-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7a892-123">-Name</span></span>
<span data-ttu-id="7a892-124">O nome da política de backup da ANF</span><span class="sxs-lookup"><span data-stu-id="7a892-124">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a892-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a892-125">-PassThru</span></span>
<span data-ttu-id="7a892-126">Retornar se a política de backup especificada foi removida com êxito</span><span class="sxs-lookup"><span data-stu-id="7a892-126">Return whether the specified backup policy was successfully removed</span></span>

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

### <span data-ttu-id="7a892-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a892-127">-ResourceGroupName</span></span>
<span data-ttu-id="7a892-128">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="7a892-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="7a892-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a892-129">-ResourceId</span></span>
<span data-ttu-id="7a892-130">A id de recurso da Política de Backup da ANF</span><span class="sxs-lookup"><span data-stu-id="7a892-130">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="7a892-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a892-131">-Confirm</span></span>
<span data-ttu-id="7a892-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a892-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a892-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a892-133">-WhatIf</span></span>
<span data-ttu-id="7a892-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7a892-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a892-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7a892-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a892-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a892-136">CommonParameters</span></span>
<span data-ttu-id="7a892-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a892-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a892-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a892-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a892-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a892-139">INPUTS</span></span>

### <span data-ttu-id="7a892-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="7a892-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="7a892-141">System.String</span><span class="sxs-lookup"><span data-stu-id="7a892-141">System.String</span></span>

### <span data-ttu-id="7a892-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="7a892-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="7a892-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7a892-143">OUTPUTS</span></span>

### <span data-ttu-id="7a892-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="7a892-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="7a892-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="7a892-145">NOTES</span></span>

## <span data-ttu-id="7a892-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a892-146">RELATED LINKS</span></span>
