---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6E886340-864C-4FF6-8FA3-669D637770F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
ms.openlocfilehash: e25cbbeb4f9920e468638bbae2ef8c53ca241fe9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602232"
---
# <span data-ttu-id="2dac7-101">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="2dac7-101">Disable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="2dac7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2dac7-102">SYNOPSIS</span></span>
<span data-ttu-id="2dac7-103">Desabilita a proteção para um item de backup protegido.</span><span class="sxs-lookup"><span data-stu-id="2dac7-103">Disables protection for a Backup protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dac7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2dac7-104">SYNTAX</span></span>

```
Disable-AzureRmBackupProtection [-RemoveRecoveryPoints] [-Force] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dac7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2dac7-105">DESCRIPTION</span></span>
<span data-ttu-id="2dac7-106">O cmdlet **Disable-AzureRmBackupProtection** desabilita a proteção para um item do Azure backup protected.</span><span class="sxs-lookup"><span data-stu-id="2dac7-106">The **Disable-AzureRmBackupProtection** cmdlet disables protection for an Azure Backup protected item.</span></span>
<span data-ttu-id="2dac7-107">Esse cmdlet para o backup agendado regular de um item.</span><span class="sxs-lookup"><span data-stu-id="2dac7-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="2dac7-108">Esse cmdlet pode excluir pontos de recuperação existentes para o item de backup.</span><span class="sxs-lookup"><span data-stu-id="2dac7-108">This cmdlet can delete existing recovery points for the backup item.</span></span>

## <span data-ttu-id="2dac7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2dac7-109">EXAMPLES</span></span>

## <span data-ttu-id="2dac7-110">OS</span><span class="sxs-lookup"><span data-stu-id="2dac7-110">PARAMETERS</span></span>

### <span data-ttu-id="2dac7-111">-Force</span><span class="sxs-lookup"><span data-stu-id="2dac7-111">-Force</span></span>
<span data-ttu-id="2dac7-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="2dac7-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2dac7-113">-Item</span><span class="sxs-lookup"><span data-stu-id="2dac7-113">-Item</span></span>
<span data-ttu-id="2dac7-114">Especifica o item de backup para o qual esse cmdlet desabilita a proteção.</span><span class="sxs-lookup"><span data-stu-id="2dac7-114">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="2dac7-115">Para obter um **AzureRmBackupItem** , use o cmdlet Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="2dac7-115">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="2dac7-116">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="2dac7-116">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="2dac7-117">Indica que esse cmdlet exclui pontos de recuperação existentes.</span><span class="sxs-lookup"><span data-stu-id="2dac7-117">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="2dac7-118">Para excluir pontos de recuperação armazenados mais tarde, execute este cmdlet novamente e especifique esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="2dac7-118">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

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

### <span data-ttu-id="2dac7-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2dac7-119">-Confirm</span></span>
<span data-ttu-id="2dac7-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dac7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dac7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dac7-121">-WhatIf</span></span>
<span data-ttu-id="2dac7-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2dac7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dac7-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2dac7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dac7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dac7-124">-DefaultProfile</span></span>
<span data-ttu-id="2dac7-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2dac7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2dac7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dac7-126">CommonParameters</span></span>
<span data-ttu-id="2dac7-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dac7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dac7-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dac7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dac7-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2dac7-129">INPUTS</span></span>

### <span data-ttu-id="2dac7-130">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="2dac7-130">AzureRmBackupItem</span></span>

## <span data-ttu-id="2dac7-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2dac7-131">OUTPUTS</span></span>

### <span data-ttu-id="2dac7-132">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="2dac7-132">AzureRmBackupJob</span></span>

## <span data-ttu-id="2dac7-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2dac7-133">NOTES</span></span>

## <span data-ttu-id="2dac7-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2dac7-134">RELATED LINKS</span></span>

[<span data-ttu-id="2dac7-135">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="2dac7-135">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="2dac7-136">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="2dac7-136">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)


