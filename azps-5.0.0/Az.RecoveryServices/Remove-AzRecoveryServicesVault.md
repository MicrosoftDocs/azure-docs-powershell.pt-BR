---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: 4e6dab95f110e25f24781b2ffbd01a016bdaa9fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118023"
---
# <span data-ttu-id="3d84c-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="3d84c-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="3d84c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d84c-102">SYNOPSIS</span></span>
<span data-ttu-id="3d84c-103">Exclui um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="3d84c-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="3d84c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d84c-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d84c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3d84c-105">DESCRIPTION</span></span>
<span data-ttu-id="3d84c-106">O cmdlet **Remove-AzRecoveryServicesVault** exclui um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="3d84c-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="3d84c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d84c-107">EXAMPLES</span></span>

### <span data-ttu-id="3d84c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3d84c-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="3d84c-109">Exclui um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="3d84c-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="3d84c-110">OS</span><span class="sxs-lookup"><span data-stu-id="3d84c-110">PARAMETERS</span></span>

### <span data-ttu-id="3d84c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d84c-111">-DefaultProfile</span></span>
<span data-ttu-id="3d84c-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d84c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d84c-113">-Cofre</span><span class="sxs-lookup"><span data-stu-id="3d84c-113">-Vault</span></span>
<span data-ttu-id="3d84c-114">Especifica um objeto do cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="3d84c-114">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="3d84c-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3d84c-115">-Confirm</span></span>
<span data-ttu-id="3d84c-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d84c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d84c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d84c-117">-WhatIf</span></span>
<span data-ttu-id="3d84c-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3d84c-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d84c-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d84c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d84c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d84c-120">CommonParameters</span></span>
<span data-ttu-id="3d84c-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d84c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d84c-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d84c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d84c-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3d84c-123">INPUTS</span></span>

### <span data-ttu-id="3d84c-124">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="3d84c-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="3d84c-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3d84c-125">OUTPUTS</span></span>

### <span data-ttu-id="3d84c-126">Microsoft. Azure. Commands. Recoveryservices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="3d84c-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="3d84c-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3d84c-127">NOTES</span></span>

## <span data-ttu-id="3d84c-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d84c-128">RELATED LINKS</span></span>

[<span data-ttu-id="3d84c-129">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="3d84c-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="3d84c-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="3d84c-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="3d84c-131">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="3d84c-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)


