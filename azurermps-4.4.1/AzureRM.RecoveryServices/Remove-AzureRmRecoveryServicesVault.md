---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: b3df84865d29bbcf62074c1b1ed7f5586fb64fee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609582"
---
# <span data-ttu-id="3609c-101">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="3609c-101">Remove-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="3609c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3609c-102">SYNOPSIS</span></span>
<span data-ttu-id="3609c-103">Exclui um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="3609c-103">Deletes a Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3609c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3609c-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3609c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3609c-105">DESCRIPTION</span></span>
<span data-ttu-id="3609c-106">O cmdlet **Remove-AzureRmRecoveryServicesVault** exclui um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="3609c-106">The **Remove-AzureRmRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="3609c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3609c-107">EXAMPLES</span></span>

## <span data-ttu-id="3609c-108">OS</span><span class="sxs-lookup"><span data-stu-id="3609c-108">PARAMETERS</span></span>

### <span data-ttu-id="3609c-109">-Cofre</span><span class="sxs-lookup"><span data-stu-id="3609c-109">-Vault</span></span>
<span data-ttu-id="3609c-110">Especifica um objeto do cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="3609c-110">Specifies an Azure Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3609c-111">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3609c-111">-Confirm</span></span>
<span data-ttu-id="3609c-112">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3609c-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3609c-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3609c-113">-WhatIf</span></span>
<span data-ttu-id="3609c-114">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3609c-114">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3609c-115">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3609c-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3609c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3609c-116">-DefaultProfile</span></span>
<span data-ttu-id="3609c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3609c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3609c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3609c-118">CommonParameters</span></span>
<span data-ttu-id="3609c-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3609c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3609c-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3609c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3609c-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3609c-121">INPUTS</span></span>

### <span data-ttu-id="3609c-122">ARSVault</span><span class="sxs-lookup"><span data-stu-id="3609c-122">ARSVault</span></span>
<span data-ttu-id="3609c-123">O parâmetro ' cofre ' aceita o valor do tipo ' ARSVault ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="3609c-123">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="3609c-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3609c-124">OUTPUTS</span></span>

### <span data-ttu-id="3609c-125">Microsoft. Azure. Commands. Recoveryservices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="3609c-125">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="3609c-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3609c-126">NOTES</span></span>

## <span data-ttu-id="3609c-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3609c-127">RELATED LINKS</span></span>

[<span data-ttu-id="3609c-128">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="3609c-128">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="3609c-129">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="3609c-129">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="3609c-130">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="3609c-130">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)


