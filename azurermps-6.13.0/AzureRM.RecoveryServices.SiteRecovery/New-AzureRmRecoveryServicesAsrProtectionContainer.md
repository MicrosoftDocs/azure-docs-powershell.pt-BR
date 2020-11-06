---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: b551e89a800c70f1321a1f58cf4d5eae39fe69e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426300"
---
# <span data-ttu-id="f9a82-101">New-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f9a82-101">New-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="f9a82-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9a82-102">SYNOPSIS</span></span>
<span data-ttu-id="f9a82-103">Cria um contêiner de proteção do Azure site Recovery dentro da malha especificada.</span><span class="sxs-lookup"><span data-stu-id="f9a82-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9a82-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9a82-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9a82-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f9a82-105">DESCRIPTION</span></span>
<span data-ttu-id="f9a82-106">O cmdlet New-AzureRmRecoveryServicesAsrProtectionContainer cria um contêiner de proteção na malha especificada do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f9a82-106">The New-AzureRmRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="f9a82-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9a82-107">EXAMPLES</span></span>

### <span data-ttu-id="f9a82-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f9a82-108">Example 1</span></span>
```
PS C:\> $job = New-AzureRmRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="f9a82-109">Inicia a criação do contêiner de proteção com os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="f9a82-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f9a82-110">OS</span><span class="sxs-lookup"><span data-stu-id="f9a82-110">PARAMETERS</span></span>

### <span data-ttu-id="f9a82-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9a82-111">-DefaultProfile</span></span>
<span data-ttu-id="f9a82-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9a82-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9a82-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9a82-113">-InputObject</span></span>
<span data-ttu-id="f9a82-114">Cria o contêiner de proteção de replicação no objeto de entrada especificado (Azure Fabric).</span><span class="sxs-lookup"><span data-stu-id="f9a82-114">Creates the replication protection container in specifed input Object (Azure Fabric).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a82-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9a82-115">-Name</span></span>
<span data-ttu-id="f9a82-116">Nome do contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="f9a82-116">Name of the protection container.</span></span>

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

### <span data-ttu-id="f9a82-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f9a82-117">-Confirm</span></span>
<span data-ttu-id="f9a82-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9a82-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9a82-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9a82-119">-WhatIf</span></span>
<span data-ttu-id="f9a82-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f9a82-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9a82-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f9a82-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9a82-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9a82-122">CommonParameters</span></span>
<span data-ttu-id="f9a82-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9a82-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9a82-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9a82-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9a82-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f9a82-125">INPUTS</span></span>

### <span data-ttu-id="f9a82-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="f9a82-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="f9a82-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f9a82-127">OUTPUTS</span></span>

### <span data-ttu-id="f9a82-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f9a82-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f9a82-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f9a82-129">NOTES</span></span>

## <span data-ttu-id="f9a82-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9a82-130">RELATED LINKS</span></span>
