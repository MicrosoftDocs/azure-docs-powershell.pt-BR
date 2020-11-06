---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 189E3DD8-AA43-4D4C-A873-971E0585E54E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 80b03c8ba4bab5968e55dff40633b014a586d450
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431162"
---
# <span data-ttu-id="38c8a-101">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="38c8a-101">Remove-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="38c8a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38c8a-102">SYNOPSIS</span></span>
<span data-ttu-id="38c8a-103">Exclui uma política de um cofre de backup.</span><span class="sxs-lookup"><span data-stu-id="38c8a-103">Deletes a policy from a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38c8a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38c8a-104">SYNTAX</span></span>

```
Remove-AzureRmBackupProtectionPolicy [-Force] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38c8a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="38c8a-105">DESCRIPTION</span></span>
<span data-ttu-id="38c8a-106">O cmdlet **Remove-AzureRmBackupProtectionPolicy** exclui uma política de um cofre de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="38c8a-106">The **Remove-AzureRmBackupProtectionPolicy** cmdlet deletes a policy from an Azure Backup vault.</span></span>

<span data-ttu-id="38c8a-107">Antes de poder excluir uma política de proteção de backup, a política não deve ter itens de backup associados.</span><span class="sxs-lookup"><span data-stu-id="38c8a-107">Before you can delete a backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="38c8a-108">Antes de excluir a política, verifique se cada item associado está associado a alguma outra política.</span><span class="sxs-lookup"><span data-stu-id="38c8a-108">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="38c8a-109">Para associar outra política a um item de backup, use o cmdlet Enable-AzureRmBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="38c8a-109">To associate another policy with a backup item, use the Enable-AzureRmBackupProtection cmdlet.</span></span>

## <span data-ttu-id="38c8a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38c8a-110">EXAMPLES</span></span>

### <span data-ttu-id="38c8a-111">Exemplo 1: remover uma política de proteção de backup</span><span class="sxs-lookup"><span data-stu-id="38c8a-111">Example 1: Remove a backup protection policy</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DailyBackup" | Remove-AzureRmBackupProtectionPolicy
```

<span data-ttu-id="38c8a-112">O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="38c8a-112">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="38c8a-113">O comando armazena esse objeto na variável $Vault.</span><span class="sxs-lookup"><span data-stu-id="38c8a-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="38c8a-114">O segundo comando cria uma política de retenção por 30 dias de retenção diária e, em seguida, armazena-a na variável $Daily.</span><span class="sxs-lookup"><span data-stu-id="38c8a-114">The second command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="38c8a-115">O segundo comando obtém a política de proteção chamada DailyBackup no cofre no $Vault usando o cmdlet **Get-AzureRmBackupProtectionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="38c8a-115">The second command gets the protection policy named DailyBackup in the vault in $Vault by using the **Get-AzureRmBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="38c8a-116">O comando passa a política para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="38c8a-116">The command passes the policy to the current cmdlet.</span></span>
<span data-ttu-id="38c8a-117">Esse cmdlet Remove a política.</span><span class="sxs-lookup"><span data-stu-id="38c8a-117">That cmdlet removes the policy.</span></span>

## <span data-ttu-id="38c8a-118">OS</span><span class="sxs-lookup"><span data-stu-id="38c8a-118">PARAMETERS</span></span>

### <span data-ttu-id="38c8a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="38c8a-119">-Force</span></span>
<span data-ttu-id="38c8a-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="38c8a-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="38c8a-121">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="38c8a-121">-ProtectionPolicy</span></span>
<span data-ttu-id="38c8a-122">Especifica a política de proteção que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="38c8a-122">Specifies protection policy that this cmdlet removes.</span></span>
<span data-ttu-id="38c8a-123">Para obter um **AzureRmBackupProtectionPolicy** , use o cmdlet Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="38c8a-123">To obtain an **AzureRmBackupProtectionPolicy** , use the Get-AzureRmBackupProtectionPolicy cmdlet</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38c8a-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="38c8a-124">-Confirm</span></span>
<span data-ttu-id="38c8a-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38c8a-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c8a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38c8a-126">-WhatIf</span></span>
<span data-ttu-id="38c8a-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="38c8a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38c8a-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="38c8a-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c8a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38c8a-129">-DefaultProfile</span></span>
<span data-ttu-id="38c8a-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38c8a-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c8a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38c8a-131">CommonParameters</span></span>
<span data-ttu-id="38c8a-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38c8a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38c8a-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38c8a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38c8a-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="38c8a-134">INPUTS</span></span>

### <span data-ttu-id="38c8a-135">AzureRMBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="38c8a-135">AzureRMBackupProtectionPolicy</span></span>

## <span data-ttu-id="38c8a-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="38c8a-136">OUTPUTS</span></span>

### <span data-ttu-id="38c8a-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="38c8a-137">None</span></span>

## <span data-ttu-id="38c8a-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="38c8a-138">NOTES</span></span>

## <span data-ttu-id="38c8a-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38c8a-139">RELATED LINKS</span></span>

[<span data-ttu-id="38c8a-140">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="38c8a-140">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="38c8a-141">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="38c8a-141">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="38c8a-142">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="38c8a-142">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


