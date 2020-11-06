---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/new-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 08166ea1ebe4c78521a68f9e5423a7947e78b699
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440298"
---
# <span data-ttu-id="e6a1c-101">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e6a1c-101">New-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="e6a1c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6a1c-102">SYNOPSIS</span></span>
<span data-ttu-id="e6a1c-103">Cria um novo cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="e6a1c-103">Creates a new Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6a1c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6a1c-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6a1c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e6a1c-105">DESCRIPTION</span></span>
<span data-ttu-id="e6a1c-106">O cmdlet **New-AzureRmRecoveryServicesVault** cria um novo cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="e6a1c-106">The **New-AzureRmRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="e6a1c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e6a1c-107">EXAMPLES</span></span>

### <span data-ttu-id="e6a1c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e6a1c-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="e6a1c-109">Criar cofre de serviços de recuperação no grupo de recursos e determinada localização.</span><span class="sxs-lookup"><span data-stu-id="e6a1c-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="e6a1c-110">OS</span><span class="sxs-lookup"><span data-stu-id="e6a1c-110">PARAMETERS</span></span>

### <span data-ttu-id="e6a1c-111">-Local</span><span class="sxs-lookup"><span data-stu-id="e6a1c-111">-Location</span></span>
<span data-ttu-id="e6a1c-112">Especifica o nome da localização geográfica do cofre.</span><span class="sxs-lookup"><span data-stu-id="e6a1c-112">Specifies the name of the geographic location of the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6a1c-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6a1c-113">-Name</span></span>
<span data-ttu-id="e6a1c-114">Especifica o nome do cofre a ser criado.</span><span class="sxs-lookup"><span data-stu-id="e6a1c-114">Specifies the name of the vault to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6a1c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6a1c-115">-ResourceGroupName</span></span>
<span data-ttu-id="e6a1c-116">Especifica o nome do grupo de recursos do Azure no qual criar ou do qual recuperar o objeto de serviços de recuperação especificado.</span><span class="sxs-lookup"><span data-stu-id="e6a1c-116">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6a1c-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e6a1c-117">-Confirm</span></span>
<span data-ttu-id="e6a1c-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6a1c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6a1c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6a1c-119">-WhatIf</span></span>
<span data-ttu-id="e6a1c-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e6a1c-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6a1c-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e6a1c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6a1c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6a1c-122">-DefaultProfile</span></span>
<span data-ttu-id="e6a1c-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e6a1c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6a1c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6a1c-124">CommonParameters</span></span>
<span data-ttu-id="e6a1c-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6a1c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6a1c-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6a1c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6a1c-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e6a1c-127">INPUTS</span></span>

### <span data-ttu-id="e6a1c-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e6a1c-128">None</span></span>

## <span data-ttu-id="e6a1c-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e6a1c-129">OUTPUTS</span></span>

### <span data-ttu-id="e6a1c-130">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="e6a1c-130">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="e6a1c-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e6a1c-131">NOTES</span></span>

## <span data-ttu-id="e6a1c-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6a1c-132">RELATED LINKS</span></span>

[<span data-ttu-id="e6a1c-133">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e6a1c-133">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="e6a1c-134">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="e6a1c-134">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="e6a1c-135">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e6a1c-135">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


