---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/remove-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 4d3046827a7d3338833b0c8c788cfb7a9e18bc2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432422"
---
# <span data-ttu-id="65657-101">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="65657-101">Remove-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="65657-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65657-102">SYNOPSIS</span></span>
<span data-ttu-id="65657-103">Exclui um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="65657-103">Deletes a Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65657-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65657-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65657-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="65657-105">DESCRIPTION</span></span>
<span data-ttu-id="65657-106">O cmdlet **Remove-AzureRmRecoveryServicesVault** exclui um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="65657-106">The **Remove-AzureRmRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="65657-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65657-107">EXAMPLES</span></span>

### <span data-ttu-id="65657-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="65657-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="65657-109">Exclui um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="65657-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="65657-110">OS</span><span class="sxs-lookup"><span data-stu-id="65657-110">PARAMETERS</span></span>

### <span data-ttu-id="65657-111">-Cofre</span><span class="sxs-lookup"><span data-stu-id="65657-111">-Vault</span></span>
<span data-ttu-id="65657-112">Especifica um objeto do cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="65657-112">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="65657-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="65657-113">-Confirm</span></span>
<span data-ttu-id="65657-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65657-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65657-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65657-115">-WhatIf</span></span>
<span data-ttu-id="65657-116">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="65657-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65657-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="65657-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65657-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65657-118">-DefaultProfile</span></span>
<span data-ttu-id="65657-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="65657-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65657-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65657-120">CommonParameters</span></span>
<span data-ttu-id="65657-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65657-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65657-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65657-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65657-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="65657-123">INPUTS</span></span>

### <span data-ttu-id="65657-124">ARSVault</span><span class="sxs-lookup"><span data-stu-id="65657-124">ARSVault</span></span>
<span data-ttu-id="65657-125">O parâmetro ' cofre ' aceita o valor do tipo ' ARSVault ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="65657-125">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="65657-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="65657-126">OUTPUTS</span></span>

### <span data-ttu-id="65657-127">Microsoft. Azure. Commands. Recoveryservices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="65657-127">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="65657-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="65657-128">NOTES</span></span>

## <span data-ttu-id="65657-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65657-129">RELATED LINKS</span></span>

[<span data-ttu-id="65657-130">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="65657-130">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="65657-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="65657-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="65657-132">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="65657-132">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)


