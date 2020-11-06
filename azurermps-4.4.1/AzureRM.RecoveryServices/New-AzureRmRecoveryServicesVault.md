---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: d9163e42b199dd5178e37a7d1bbe22abbb05c7f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427814"
---
# <span data-ttu-id="53ee1-101">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="53ee1-101">New-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="53ee1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53ee1-102">SYNOPSIS</span></span>
<span data-ttu-id="53ee1-103">Cria um novo cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="53ee1-103">Creates a new Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53ee1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53ee1-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53ee1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53ee1-105">DESCRIPTION</span></span>
<span data-ttu-id="53ee1-106">O cmdlet **New-AzureRmRecoveryServicesVault** cria um novo cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="53ee1-106">The **New-AzureRmRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="53ee1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53ee1-107">EXAMPLES</span></span>

## <span data-ttu-id="53ee1-108">OS</span><span class="sxs-lookup"><span data-stu-id="53ee1-108">PARAMETERS</span></span>

### <span data-ttu-id="53ee1-109">-Local</span><span class="sxs-lookup"><span data-stu-id="53ee1-109">-Location</span></span>
<span data-ttu-id="53ee1-110">Especifica o nome da localização geográfica do cofre.</span><span class="sxs-lookup"><span data-stu-id="53ee1-110">Specifies the name of the geographic location of the vault.</span></span>

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

### <span data-ttu-id="53ee1-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="53ee1-111">-Name</span></span>
<span data-ttu-id="53ee1-112">Especifica o nome do cofre a ser criado.</span><span class="sxs-lookup"><span data-stu-id="53ee1-112">Specifies the name of the vault to create.</span></span>

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

### <span data-ttu-id="53ee1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53ee1-113">-ResourceGroupName</span></span>
<span data-ttu-id="53ee1-114">Especifica o nome do grupo de recursos do Azure no qual criar ou do qual recuperar o objeto de serviços de recuperação especificado.</span><span class="sxs-lookup"><span data-stu-id="53ee1-114">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="53ee1-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="53ee1-115">-Confirm</span></span>
<span data-ttu-id="53ee1-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53ee1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53ee1-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53ee1-117">-WhatIf</span></span>
<span data-ttu-id="53ee1-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="53ee1-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53ee1-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="53ee1-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53ee1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53ee1-120">-DefaultProfile</span></span>
<span data-ttu-id="53ee1-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="53ee1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53ee1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53ee1-122">CommonParameters</span></span>
<span data-ttu-id="53ee1-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53ee1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53ee1-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53ee1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53ee1-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53ee1-125">INPUTS</span></span>

## <span data-ttu-id="53ee1-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53ee1-126">OUTPUTS</span></span>

### <span data-ttu-id="53ee1-127">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="53ee1-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="53ee1-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53ee1-128">NOTES</span></span>

## <span data-ttu-id="53ee1-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53ee1-129">RELATED LINKS</span></span>

[<span data-ttu-id="53ee1-130">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="53ee1-130">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="53ee1-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="53ee1-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="53ee1-132">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="53ee1-132">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)

