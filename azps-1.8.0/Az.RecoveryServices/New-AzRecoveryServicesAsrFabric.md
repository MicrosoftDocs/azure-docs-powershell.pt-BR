---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 8604d1a648590e0fc88a268e6bf2941bbf9344e1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599672"
---
# <span data-ttu-id="1c8d8-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="1c8d8-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="1c8d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c8d8-102">SYNOPSIS</span></span>
<span data-ttu-id="1c8d8-103">Cria uma malha do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1c8d8-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="1c8d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c8d8-104">SYNTAX</span></span>

### <span data-ttu-id="1c8d8-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="1c8d8-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c8d8-106">Azure</span><span class="sxs-lookup"><span data-stu-id="1c8d8-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c8d8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c8d8-107">DESCRIPTION</span></span>
<span data-ttu-id="1c8d8-108">O cmdlet **New-AzRecoveryServicesAsrFabric** cria uma malha de recuperação de site do Azure do tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="1c8d8-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="1c8d8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c8d8-109">EXAMPLES</span></span>

### <span data-ttu-id="1c8d8-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1c8d8-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="1c8d8-111">Inicia a criação do Fabric com o nome passado e retorna o trabalho ASR usado para acompanhar a operação de criação do fabric.</span><span class="sxs-lookup"><span data-stu-id="1c8d8-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="1c8d8-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1c8d8-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Az -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="1c8d8-113">Inicia a criação do Azure Fabric com o nome passado e retorna o trabalho ASR usado para acompanhar a operação de criação do fabric.</span><span class="sxs-lookup"><span data-stu-id="1c8d8-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="1c8d8-114">OS</span><span class="sxs-lookup"><span data-stu-id="1c8d8-114">PARAMETERS</span></span>

### <span data-ttu-id="1c8d8-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="1c8d8-115">-Azure</span></span>
<span data-ttu-id="1c8d8-116">{{Preencher descrição do Azure}}</span><span class="sxs-lookup"><span data-stu-id="1c8d8-116">{{Fill Azure Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c8d8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c8d8-117">-DefaultProfile</span></span>
<span data-ttu-id="1c8d8-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c8d8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1c8d8-119">-Local</span><span class="sxs-lookup"><span data-stu-id="1c8d8-119">-Location</span></span>
<span data-ttu-id="1c8d8-120">Especifica a região do Azure correspondente ao objeto Fabric que está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="1c8d8-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="1c8d8-121">O objeto de malha do Azure site Recovery representa uma região.</span><span class="sxs-lookup"><span data-stu-id="1c8d8-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="1c8d8-122">Para máquinas virtuais sendo replicadas entre duas regiões do Azure, uma malha primária representa a região principal do Azure e a malha de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1c8d8-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

```yaml
Type: System.String
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c8d8-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c8d8-123">-Name</span></span>
<span data-ttu-id="1c8d8-124">Especifica o nome da malha de recuperação do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="1c8d8-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="1c8d8-125">-Digite</span><span class="sxs-lookup"><span data-stu-id="1c8d8-125">-Type</span></span>
<span data-ttu-id="1c8d8-126">Especifica o tipo de malha do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1c8d8-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c8d8-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1c8d8-127">-Confirm</span></span>
<span data-ttu-id="1c8d8-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c8d8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c8d8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c8d8-129">-WhatIf</span></span>
<span data-ttu-id="1c8d8-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1c8d8-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c8d8-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1c8d8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c8d8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c8d8-132">CommonParameters</span></span>
<span data-ttu-id="1c8d8-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c8d8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c8d8-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c8d8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c8d8-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c8d8-135">INPUTS</span></span>

### <span data-ttu-id="1c8d8-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1c8d8-136">None</span></span>

## <span data-ttu-id="1c8d8-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c8d8-137">OUTPUTS</span></span>

### <span data-ttu-id="1c8d8-138">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1c8d8-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1c8d8-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c8d8-139">NOTES</span></span>

## <span data-ttu-id="1c8d8-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c8d8-140">RELATED LINKS</span></span>

[<span data-ttu-id="1c8d8-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="1c8d8-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="1c8d8-142">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="1c8d8-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
