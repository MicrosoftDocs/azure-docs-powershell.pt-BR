---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/set-azurermrecoveryservicesbackupproperties
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
ms.openlocfilehash: d8512567a7dd094f14c4bb49a7f575dd13341d10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432421"
---
# <span data-ttu-id="ef06f-101">Set-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="ef06f-101">Set-AzureRmRecoveryServicesBackupProperties</span></span>

## <span data-ttu-id="ef06f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ef06f-102">SYNOPSIS</span></span>
<span data-ttu-id="ef06f-103">Define as propriedades do gerenciamento de backup.</span><span class="sxs-lookup"><span data-stu-id="ef06f-103">Sets the properties for backup management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef06f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef06f-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProperties -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef06f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ef06f-105">DESCRIPTION</span></span>
<span data-ttu-id="ef06f-106">O cmdlet **set-AzureRmRecoveryServicesBackupProperties** define as propriedades de armazenamento de backup para um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="ef06f-106">The **Set-AzureRmRecoveryServicesBackupProperties** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="ef06f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef06f-107">EXAMPLES</span></span>

### <span data-ttu-id="ef06f-108">Exemplo 1: definir o armazenamento georedundante para um cofre</span><span class="sxs-lookup"><span data-stu-id="ef06f-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzureRmRecoveryServicesBackupProperties -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="ef06f-109">O primeiro comando obtém o cofre chamado TestVault e, em seguida, armazena-o na variável $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="ef06f-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>

<span data-ttu-id="ef06f-110">O segundo comando define a redundância de armazenamento de backup para $Vault 01 a georedundante.</span><span class="sxs-lookup"><span data-stu-id="ef06f-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="ef06f-111">OS</span><span class="sxs-lookup"><span data-stu-id="ef06f-111">PARAMETERS</span></span>

### <span data-ttu-id="ef06f-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="ef06f-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="ef06f-113">Especifica o tipo de redundância do armazenamento de backup.</span><span class="sxs-lookup"><span data-stu-id="ef06f-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: AzureRmRecoveryServicesBackupStorageRedundancyType
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef06f-114">-Cofre</span><span class="sxs-lookup"><span data-stu-id="ef06f-114">-Vault</span></span>
<span data-ttu-id="ef06f-115">Especifica o nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="ef06f-115">Specifies the name of the vault.</span></span>
<span data-ttu-id="ef06f-116">O cofre deve ser um objeto **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="ef06f-116">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef06f-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ef06f-117">-Confirm</span></span>
<span data-ttu-id="ef06f-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef06f-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef06f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef06f-119">-WhatIf</span></span>
<span data-ttu-id="ef06f-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ef06f-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef06f-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ef06f-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef06f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef06f-122">-DefaultProfile</span></span>
<span data-ttu-id="ef06f-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ef06f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef06f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef06f-124">CommonParameters</span></span>
<span data-ttu-id="ef06f-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef06f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef06f-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef06f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef06f-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ef06f-127">INPUTS</span></span>

### <span data-ttu-id="ef06f-128">ARSVault</span><span class="sxs-lookup"><span data-stu-id="ef06f-128">ARSVault</span></span>
<span data-ttu-id="ef06f-129">O parâmetro ' cofre ' aceita o valor do tipo ' ARSVault ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="ef06f-129">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="ef06f-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ef06f-130">OUTPUTS</span></span>

## <span data-ttu-id="ef06f-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ef06f-131">NOTES</span></span>

## <span data-ttu-id="ef06f-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef06f-132">RELATED LINKS</span></span>

[<span data-ttu-id="ef06f-133">Get-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="ef06f-133">Get-AzureRmRecoveryServicesBackupProperties</span></span>](./Get-AzureRmRecoveryServicesBackupProperties.md)

[<span data-ttu-id="ef06f-134">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ef06f-134">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

