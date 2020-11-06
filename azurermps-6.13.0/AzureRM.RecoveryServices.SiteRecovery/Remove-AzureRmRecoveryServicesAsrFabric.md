---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 8a7b36b67b0ec1721da36dfeba920b556892c5f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440042"
---
# <span data-ttu-id="8a363-101">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="8a363-101">Remove-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="8a363-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8a363-102">SYNOPSIS</span></span>
<span data-ttu-id="8a363-103">Exclui a malha de recuperação de site do Azure especificada do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8a363-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a363-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a363-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a363-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8a363-105">DESCRIPTION</span></span>
<span data-ttu-id="8a363-106">O cmdlet **Remove-AzureRmRecoveryServicesAsrFabric** remove a estrutura de recuperação de site do Azure especificada do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8a363-106">The **Remove-AzureRmRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="8a363-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8a363-107">EXAMPLES</span></span>

### <span data-ttu-id="8a363-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8a363-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="8a363-109">Inicia a exclusão da malha especificada e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="8a363-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8a363-110">OS</span><span class="sxs-lookup"><span data-stu-id="8a363-110">PARAMETERS</span></span>

### <span data-ttu-id="8a363-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a363-111">-DefaultProfile</span></span>
<span data-ttu-id="8a363-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8a363-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8a363-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8a363-113">-Force</span></span>
<span data-ttu-id="8a363-114">Force o comando a ser executado sem fornecer um aviso adicional.</span><span class="sxs-lookup"><span data-stu-id="8a363-114">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a363-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a363-115">-InputObject</span></span>
<span data-ttu-id="8a363-116">O objeto de entrada para o cmdlet: o objeto de malha ASR correspondente à malha a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="8a363-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

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

### <span data-ttu-id="8a363-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8a363-117">-Confirm</span></span>
<span data-ttu-id="8a363-118">Especifique se a confirmação é necessária.</span><span class="sxs-lookup"><span data-stu-id="8a363-118">Specify if confirmation is required.</span></span> <span data-ttu-id="8a363-119">Defina o valor do parâmetro Confirm para $false a fim de ignorar a confirmação.</span><span class="sxs-lookup"><span data-stu-id="8a363-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="8a363-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a363-120">-WhatIf</span></span>
<span data-ttu-id="8a363-121">Mostra o que aconteceria se o cmdlet fosse executado sem realmente executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a363-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="8a363-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a363-122">CommonParameters</span></span>
<span data-ttu-id="8a363-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a363-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a363-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a363-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a363-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8a363-125">INPUTS</span></span>

### <span data-ttu-id="8a363-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="8a363-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="8a363-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8a363-127">OUTPUTS</span></span>

### <span data-ttu-id="8a363-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8a363-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8a363-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8a363-129">NOTES</span></span>

## <span data-ttu-id="8a363-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a363-130">RELATED LINKS</span></span>

[<span data-ttu-id="8a363-131">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="8a363-131">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="8a363-132">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="8a363-132">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)
