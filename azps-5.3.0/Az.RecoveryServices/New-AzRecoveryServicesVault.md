---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
ms.openlocfilehash: 3bb602d148b0843def129a1e4538d9ef8fdbe169
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428791"
---
# <span data-ttu-id="541fa-101">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="541fa-101">New-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="541fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="541fa-102">SYNOPSIS</span></span>
<span data-ttu-id="541fa-103">Cria um novo cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="541fa-103">Creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="541fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="541fa-104">SYNTAX</span></span>

```
New-AzRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="541fa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="541fa-105">DESCRIPTION</span></span>
<span data-ttu-id="541fa-106">O cmdlet **New-AzRecoveryServicesVault** cria um novo cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="541fa-106">The **New-AzRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="541fa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="541fa-107">EXAMPLES</span></span>

### <span data-ttu-id="541fa-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="541fa-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="541fa-109">Criar cofre de serviços de recuperação no grupo de recursos e determinada localização.</span><span class="sxs-lookup"><span data-stu-id="541fa-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="541fa-110">OS</span><span class="sxs-lookup"><span data-stu-id="541fa-110">PARAMETERS</span></span>

### <span data-ttu-id="541fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="541fa-111">-DefaultProfile</span></span>
<span data-ttu-id="541fa-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="541fa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="541fa-113">-Local</span><span class="sxs-lookup"><span data-stu-id="541fa-113">-Location</span></span>
<span data-ttu-id="541fa-114">Especifica o nome da localização geográfica do cofre.</span><span class="sxs-lookup"><span data-stu-id="541fa-114">Specifies the name of the geographic location of the vault.</span></span>

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

### <span data-ttu-id="541fa-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="541fa-115">-Name</span></span>
<span data-ttu-id="541fa-116">Especifica o nome do cofre a ser criado.</span><span class="sxs-lookup"><span data-stu-id="541fa-116">Specifies the name of the vault to create.</span></span>

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

### <span data-ttu-id="541fa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="541fa-117">-ResourceGroupName</span></span>
<span data-ttu-id="541fa-118">Especifica o nome do grupo de recursos do Azure no qual criar ou do qual recuperar o objeto de serviços de recuperação especificado.</span><span class="sxs-lookup"><span data-stu-id="541fa-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="541fa-119">-Marca</span><span class="sxs-lookup"><span data-stu-id="541fa-119">-Tag</span></span>

<span data-ttu-id="541fa-120">Especifica as marcas a serem adicionadas ao cofre de serviços de recuperação</span><span class="sxs-lookup"><span data-stu-id="541fa-120">Specifies the Tags to add to the Recovery Services Vault</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="541fa-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="541fa-121">-Confirm</span></span>
<span data-ttu-id="541fa-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="541fa-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="541fa-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="541fa-123">-WhatIf</span></span>
<span data-ttu-id="541fa-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="541fa-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="541fa-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="541fa-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="541fa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="541fa-126">CommonParameters</span></span>
<span data-ttu-id="541fa-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="541fa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="541fa-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="541fa-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="541fa-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="541fa-129">INPUTS</span></span>

### <span data-ttu-id="541fa-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="541fa-130">None</span></span>

## <span data-ttu-id="541fa-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="541fa-131">OUTPUTS</span></span>

### <span data-ttu-id="541fa-132">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="541fa-132">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="541fa-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="541fa-133">NOTES</span></span>

## <span data-ttu-id="541fa-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="541fa-134">RELATED LINKS</span></span>

[<span data-ttu-id="541fa-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="541fa-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="541fa-136">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="541fa-136">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="541fa-137">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="541fa-137">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


