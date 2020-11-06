---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 53398a882ff513443f8eae336539858f7fe34ce4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431647"
---
# <span data-ttu-id="4dcf1-101">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="4dcf1-101">New-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="4dcf1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4dcf1-102">SYNOPSIS</span></span>
<span data-ttu-id="4dcf1-103">Cria uma malha do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4dcf1-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4dcf1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4dcf1-104">SYNTAX</span></span>

### <span data-ttu-id="4dcf1-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="4dcf1-105">Default (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dcf1-106">Azure</span><span class="sxs-lookup"><span data-stu-id="4dcf1-106">Azure</span></span>
```
New-AzureRmRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dcf1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4dcf1-107">DESCRIPTION</span></span>
<span data-ttu-id="4dcf1-108">O cmdlet **New-AzureRmRecoveryServicesAsrFabric** cria uma malha de recuperação de site do Azure do tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="4dcf1-108">The **New-AzureRmRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="4dcf1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4dcf1-109">EXAMPLES</span></span>

### <span data-ttu-id="4dcf1-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4dcf1-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="4dcf1-111">Inicia a criação do Fabric com o nome passado e retorna o trabalho ASR usado para acompanhar a operação de criação do fabric.</span><span class="sxs-lookup"><span data-stu-id="4dcf1-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="4dcf1-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4dcf1-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="4dcf1-113">Inicia a criação do Azure Fabric com o nome passado e retorna o trabalho ASR usado para acompanhar a operação de criação do fabric.</span><span class="sxs-lookup"><span data-stu-id="4dcf1-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="4dcf1-114">OS</span><span class="sxs-lookup"><span data-stu-id="4dcf1-114">PARAMETERS</span></span>

### <span data-ttu-id="4dcf1-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="4dcf1-115">-Azure</span></span>
<span data-ttu-id="4dcf1-116">Parâmetro de opção indica a criação da malha do Azure.</span><span class="sxs-lookup"><span data-stu-id="4dcf1-116">Switch parameter indicates creation of azure fabric.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dcf1-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4dcf1-117">-Confirm</span></span>
<span data-ttu-id="4dcf1-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dcf1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dcf1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dcf1-119">-DefaultProfile</span></span>
<span data-ttu-id="4dcf1-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4dcf1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="4dcf1-121">-Local</span><span class="sxs-lookup"><span data-stu-id="4dcf1-121">-Location</span></span>
<span data-ttu-id="4dcf1-122">Especifica a região do Azure correspondente ao objeto Fabric que está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="4dcf1-122">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="4dcf1-123">O objeto de malha do Azure site Recovery representa uma região.</span><span class="sxs-lookup"><span data-stu-id="4dcf1-123">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="4dcf1-124">Para máquinas virtuais sendo replicadas entre duas regiões do Azure, uma malha primária representa a região principal do Azure e a malha de recuperação.</span><span class="sxs-lookup"><span data-stu-id="4dcf1-124">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

```yaml
Type: String
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dcf1-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="4dcf1-125">-Name</span></span>
<span data-ttu-id="4dcf1-126">Especifica o nome da malha de recuperação do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="4dcf1-126">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="4dcf1-127">-Digite</span><span class="sxs-lookup"><span data-stu-id="4dcf1-127">-Type</span></span>
<span data-ttu-id="4dcf1-128">Especifica o tipo de malha do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4dcf1-128">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dcf1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dcf1-129">-WhatIf</span></span>
<span data-ttu-id="4dcf1-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4dcf1-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4dcf1-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4dcf1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dcf1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dcf1-132">CommonParameters</span></span>
<span data-ttu-id="4dcf1-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dcf1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dcf1-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dcf1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dcf1-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4dcf1-135">INPUTS</span></span>

### <span data-ttu-id="4dcf1-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4dcf1-136">None</span></span>

## <span data-ttu-id="4dcf1-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4dcf1-137">OUTPUTS</span></span>

### <span data-ttu-id="4dcf1-138">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4dcf1-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4dcf1-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4dcf1-139">NOTES</span></span>

## <span data-ttu-id="4dcf1-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4dcf1-140">RELATED LINKS</span></span>

[<span data-ttu-id="4dcf1-141">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="4dcf1-141">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="4dcf1-142">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="4dcf1-142">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
