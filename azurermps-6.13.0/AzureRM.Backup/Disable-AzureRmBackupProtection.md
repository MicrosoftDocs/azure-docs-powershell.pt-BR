---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6E886340-864C-4FF6-8FA3-669D637770F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/disable-azurermbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
ms.openlocfilehash: ebea82628aae6df23d16a341f3fd503870a8037a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433323"
---
# <span data-ttu-id="d2267-101">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="d2267-101">Disable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="d2267-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2267-102">SYNOPSIS</span></span>
<span data-ttu-id="d2267-103">Desabilita a proteção para um item de backup protegido.</span><span class="sxs-lookup"><span data-stu-id="d2267-103">Disables protection for a Backup protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2267-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2267-104">SYNTAX</span></span>

```
Disable-AzureRmBackupProtection [-RemoveRecoveryPoints] [-Force] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2267-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2267-105">DESCRIPTION</span></span>
<span data-ttu-id="d2267-106">O cmdlet **Disable-AzureRmBackupProtection** desabilita a proteção para um item do Azure backup protected.</span><span class="sxs-lookup"><span data-stu-id="d2267-106">The **Disable-AzureRmBackupProtection** cmdlet disables protection for an Azure Backup protected item.</span></span>
<span data-ttu-id="d2267-107">Esse cmdlet para o backup agendado regular de um item.</span><span class="sxs-lookup"><span data-stu-id="d2267-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="d2267-108">Esse cmdlet pode excluir pontos de recuperação existentes para o item de backup.</span><span class="sxs-lookup"><span data-stu-id="d2267-108">This cmdlet can delete existing recovery points for the backup item.</span></span>

## <span data-ttu-id="d2267-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2267-109">EXAMPLES</span></span>

## <span data-ttu-id="d2267-110">OS</span><span class="sxs-lookup"><span data-stu-id="d2267-110">PARAMETERS</span></span>

### <span data-ttu-id="d2267-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2267-111">-DefaultProfile</span></span>
<span data-ttu-id="d2267-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d2267-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2267-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d2267-113">-Force</span></span>
<span data-ttu-id="d2267-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="d2267-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d2267-115">-Item</span><span class="sxs-lookup"><span data-stu-id="d2267-115">-Item</span></span>
<span data-ttu-id="d2267-116">Especifica o item de backup para o qual esse cmdlet desabilita a proteção.</span><span class="sxs-lookup"><span data-stu-id="d2267-116">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="d2267-117">Para obter um **AzureRmBackupItem** , use o cmdlet Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="d2267-117">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2267-118">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="d2267-118">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="d2267-119">Indica que esse cmdlet exclui pontos de recuperação existentes.</span><span class="sxs-lookup"><span data-stu-id="d2267-119">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="d2267-120">Para excluir pontos de recuperação armazenados mais tarde, execute este cmdlet novamente e especifique esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d2267-120">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2267-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d2267-121">-Confirm</span></span>
<span data-ttu-id="d2267-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2267-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2267-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2267-123">-WhatIf</span></span>
<span data-ttu-id="d2267-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2267-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2267-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2267-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2267-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2267-126">CommonParameters</span></span>
<span data-ttu-id="d2267-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2267-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2267-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2267-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2267-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2267-129">INPUTS</span></span>

### <span data-ttu-id="d2267-130">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupItem</span><span class="sxs-lookup"><span data-stu-id="d2267-130">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem</span></span>
<span data-ttu-id="d2267-131">Parâmetros: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d2267-131">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="d2267-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2267-132">OUTPUTS</span></span>

### <span data-ttu-id="d2267-133">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="d2267-133">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="d2267-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2267-134">NOTES</span></span>

## <span data-ttu-id="d2267-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2267-135">RELATED LINKS</span></span>

[<span data-ttu-id="d2267-136">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="d2267-136">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="d2267-137">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="d2267-137">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

