---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 542e75ed0e6531f5778f9793b678b42f953c15d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426658"
---
# <span data-ttu-id="4b481-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="4b481-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="4b481-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b481-102">SYNOPSIS</span></span>
<span data-ttu-id="4b481-103">Cria um objeto de mapeamento de disco para discos de máquina virtual do Azure a serem replicados.</span><span class="sxs-lookup"><span data-stu-id="4b481-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b481-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b481-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b481-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b481-105">DESCRIPTION</span></span>
<span data-ttu-id="4b481-106">Cria um objeto de mapeamento de disco que mapeia um disco da máquina virtual do Azure para a conta de armazenamento do cache e a conta de armazenamento de destino (região de recuperação) a ser usada para replicar o disco.</span><span class="sxs-lookup"><span data-stu-id="4b481-106">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="4b481-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b481-107">EXAMPLES</span></span>

### <span data-ttu-id="4b481-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4b481-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="4b481-109">Crie um objeto de mapeamento de disco para discos de máquina virtual do Azure a serem replicados. Usado durante a operação do Azure to Azure EnableD e do reprotect.</span><span class="sxs-lookup"><span data-stu-id="4b481-109">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="4b481-110">OS</span><span class="sxs-lookup"><span data-stu-id="4b481-110">PARAMETERS</span></span>

### <span data-ttu-id="4b481-111">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4b481-111">-Confirm</span></span>
<span data-ttu-id="4b481-112">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b481-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b481-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b481-113">-DefaultProfile</span></span>
<span data-ttu-id="4b481-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b481-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b481-115">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4b481-115">-LogStorageAccountId</span></span>
<span data-ttu-id="4b481-116">Especifica o log ou a ID da conta de armazenamento do cache a ser usada para armazenar logs de replicação.</span><span class="sxs-lookup"><span data-stu-id="4b481-116">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="4b481-117">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4b481-117">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="4b481-118">Especifica a ID da conta de armazenamento do Azure a ser replicada.</span><span class="sxs-lookup"><span data-stu-id="4b481-118">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="4b481-119">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="4b481-119">-VhdUri</span></span>
<span data-ttu-id="4b481-120">Especifique o URI do VHD do disco ao qual esse mapeamento corresponde.</span><span class="sxs-lookup"><span data-stu-id="4b481-120">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="4b481-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b481-121">-WhatIf</span></span>
<span data-ttu-id="4b481-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4b481-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b481-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4b481-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b481-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b481-124">CommonParameters</span></span>
<span data-ttu-id="4b481-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b481-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b481-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b481-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b481-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b481-127">INPUTS</span></span>

### <span data-ttu-id="4b481-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4b481-128">None</span></span>

## <span data-ttu-id="4b481-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b481-129">OUTPUTS</span></span>

### <span data-ttu-id="4b481-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="4b481-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="4b481-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b481-131">NOTES</span></span>

## <span data-ttu-id="4b481-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b481-132">RELATED LINKS</span></span>
