---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6E886340-864C-4FF6-8FA3-669D637770F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/disable-azurermbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
ms.openlocfilehash: cd3f5520b688d5a83cae20216fac47e9120b4cc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609526"
---
# <span data-ttu-id="26849-101">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="26849-101">Disable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="26849-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="26849-102">SYNOPSIS</span></span>
<span data-ttu-id="26849-103">Desabilita a proteção para um item de backup protegido.</span><span class="sxs-lookup"><span data-stu-id="26849-103">Disables protection for a Backup protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26849-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26849-104">SYNTAX</span></span>

```
Disable-AzureRmBackupProtection [-RemoveRecoveryPoints] [-Force] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26849-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="26849-105">DESCRIPTION</span></span>
<span data-ttu-id="26849-106">O cmdlet **Disable-AzureRmBackupProtection** desabilita a proteção para um item do Azure backup protected.</span><span class="sxs-lookup"><span data-stu-id="26849-106">The **Disable-AzureRmBackupProtection** cmdlet disables protection for an Azure Backup protected item.</span></span>
<span data-ttu-id="26849-107">Esse cmdlet para o backup agendado regular de um item.</span><span class="sxs-lookup"><span data-stu-id="26849-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="26849-108">Esse cmdlet pode excluir pontos de recuperação existentes para o item de backup.</span><span class="sxs-lookup"><span data-stu-id="26849-108">This cmdlet can delete existing recovery points for the backup item.</span></span>

## <span data-ttu-id="26849-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="26849-109">EXAMPLES</span></span>

## <span data-ttu-id="26849-110">OS</span><span class="sxs-lookup"><span data-stu-id="26849-110">PARAMETERS</span></span>

### <span data-ttu-id="26849-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26849-111">-DefaultProfile</span></span>
<span data-ttu-id="26849-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="26849-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26849-113">-Force</span><span class="sxs-lookup"><span data-stu-id="26849-113">-Force</span></span>
<span data-ttu-id="26849-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="26849-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26849-115">-Item</span><span class="sxs-lookup"><span data-stu-id="26849-115">-Item</span></span>
<span data-ttu-id="26849-116">Especifica o item de backup para o qual esse cmdlet desabilita a proteção.</span><span class="sxs-lookup"><span data-stu-id="26849-116">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="26849-117">Para obter um **AzureRmBackupItem** , use o cmdlet Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="26849-117">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: AzureRMBackupItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26849-118">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="26849-118">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="26849-119">Indica que esse cmdlet exclui pontos de recuperação existentes.</span><span class="sxs-lookup"><span data-stu-id="26849-119">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="26849-120">Para excluir pontos de recuperação armazenados mais tarde, execute este cmdlet novamente e especifique esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="26849-120">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26849-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="26849-121">-Confirm</span></span>
<span data-ttu-id="26849-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26849-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26849-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26849-123">-WhatIf</span></span>
<span data-ttu-id="26849-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="26849-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26849-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="26849-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26849-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26849-126">CommonParameters</span></span>
<span data-ttu-id="26849-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26849-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26849-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26849-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26849-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="26849-129">INPUTS</span></span>

### <span data-ttu-id="26849-130">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="26849-130">AzureRmBackupItem</span></span>

## <span data-ttu-id="26849-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="26849-131">OUTPUTS</span></span>

### <span data-ttu-id="26849-132">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="26849-132">AzureRmBackupJob</span></span>

## <span data-ttu-id="26849-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="26849-133">NOTES</span></span>

## <span data-ttu-id="26849-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26849-134">RELATED LINKS</span></span>

[<span data-ttu-id="26849-135">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="26849-135">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="26849-136">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="26849-136">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)


