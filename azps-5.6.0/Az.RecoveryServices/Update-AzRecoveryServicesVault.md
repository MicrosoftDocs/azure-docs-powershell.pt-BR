---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
ms.openlocfilehash: 104bb05b4a01f5407c56e6c89de632a1ec5ab475
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887636"
---
# <span data-ttu-id="6e8af-101">Update-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="6e8af-101">Update-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="6e8af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e8af-102">SYNOPSIS</span></span>
<span data-ttu-id="6e8af-103">Atualiza o MSI para o cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="6e8af-103">Updates MSI to the recovery services vault.</span></span>

## <span data-ttu-id="6e8af-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6e8af-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesVault -ResourceGroupName <string> -Name <string> -IdentityType <MSIdentity>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e8af-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6e8af-105">DESCRIPTION</span></span>
<span data-ttu-id="6e8af-106">Esse cmdlet é usado para adicionar ou remover o MSI do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="6e8af-106">This cmdlet is used to add or remove  the MSI from the recovery services vault.</span></span> <span data-ttu-id="6e8af-107">Use -IdentityType para atribuir uma identidade SystemAssigned ao RSVault.</span><span class="sxs-lookup"><span data-stu-id="6e8af-107">Use -IdentityType param to assign a SystemAssigned identity to the RSVault.</span></span> <span data-ttu-id="6e8af-108">Use IdentityType None para remover o MSI do cofre.</span><span class="sxs-lookup"><span data-stu-id="6e8af-108">Use IdentityType None to remove the MSI from the vault.</span></span>

## <span data-ttu-id="6e8af-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e8af-109">EXAMPLES</span></span>

### <span data-ttu-id="6e8af-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6e8af-110">Example 1</span></span>
```powershell
PS C:\> Update-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName" -IdentityType SystemAssigned
```

<span data-ttu-id="6e8af-111">Esse cmdlet é usado para adicionar uma identidade SystemAssigned a um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="6e8af-111">This cmdlet is used to add a SystemAssigned identity to a recovery services vault.</span></span>

## <span data-ttu-id="6e8af-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6e8af-112">PARAMETERS</span></span>

### <span data-ttu-id="6e8af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e8af-113">-DefaultProfile</span></span>
<span data-ttu-id="6e8af-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6e8af-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e8af-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6e8af-115">-Name</span></span>

<span data-ttu-id="6e8af-116">Especifica o nome do cofre de serviços de recuperação a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="6e8af-116">Specifies the name of the recovery services vault to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e8af-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e8af-117">-ResourceGroupName</span></span>

<span data-ttu-id="6e8af-118">Especifica o nome do grupo de recursos do Azure onde o cofre de serviços de recuperação está presente.</span><span class="sxs-lookup"><span data-stu-id="6e8af-118">Specifies the name of the Azure resource group where recovery services vault is present.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e8af-119">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="6e8af-119">-IdentityType</span></span>
<span data-ttu-id="6e8af-120">O tipo MSI atribuído ao Recovery Services Vault.</span><span class="sxs-lookup"><span data-stu-id="6e8af-120">The MSI type assigned to Recovery Services Vault.</span></span>

```yaml
Type: MSIdentity
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e8af-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e8af-121">-Confirm</span></span>
<span data-ttu-id="6e8af-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e8af-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e8af-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e8af-123">-WhatIf</span></span>
<span data-ttu-id="6e8af-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6e8af-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e8af-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6e8af-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e8af-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e8af-126">CommonParameters</span></span>
<span data-ttu-id="6e8af-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e8af-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e8af-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e8af-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e8af-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e8af-129">INPUTS</span></span>

### <span data-ttu-id="6e8af-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6e8af-130">System.String</span></span>

## <span data-ttu-id="6e8af-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6e8af-131">OUTPUTS</span></span>

### <span data-ttu-id="6e8af-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span><span class="sxs-lookup"><span data-stu-id="6e8af-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span></span>

## <span data-ttu-id="6e8af-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="6e8af-133">NOTES</span></span>

## <span data-ttu-id="6e8af-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e8af-134">RELATED LINKS</span></span>
