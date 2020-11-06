---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 56c188b6b6e902fffa9cd777d6a5acf3b38cb2fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428399"
---
# <span data-ttu-id="56d9b-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="56d9b-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="56d9b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="56d9b-102">SYNOPSIS</span></span>
<span data-ttu-id="56d9b-103">Exclui o mapeamento de rede ASR especificado do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="56d9b-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56d9b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56d9b-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56d9b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="56d9b-105">DESCRIPTION</span></span>
<span data-ttu-id="56d9b-106">O cmdlet **Remove-AzureRmRecoveryServicesAsrNetworkMapping** exclui o mapeamento de rede ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="56d9b-106">The **Remove-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="56d9b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56d9b-107">EXAMPLES</span></span>

### <span data-ttu-id="56d9b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="56d9b-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="56d9b-109">Inicia a exclusão do mapeamento de rede ASR especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="56d9b-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="56d9b-110">OS</span><span class="sxs-lookup"><span data-stu-id="56d9b-110">PARAMETERS</span></span>

### <span data-ttu-id="56d9b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56d9b-111">-DefaultProfile</span></span>
<span data-ttu-id="56d9b-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="56d9b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="56d9b-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56d9b-113">-InputObject</span></span>
<span data-ttu-id="56d9b-114">O objeto de entrada para o cmdlet: o objeto de mapeamento de rede ASR correspondente ao mapeamento de rede ASR a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="56d9b-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56d9b-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="56d9b-115">-Confirm</span></span>
<span data-ttu-id="56d9b-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56d9b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56d9b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56d9b-117">-WhatIf</span></span>
<span data-ttu-id="56d9b-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="56d9b-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56d9b-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="56d9b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56d9b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d9b-120">CommonParameters</span></span>
<span data-ttu-id="56d9b-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56d9b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d9b-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56d9b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d9b-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="56d9b-123">INPUTS</span></span>

### <span data-ttu-id="56d9b-124">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="56d9b-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="56d9b-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="56d9b-125">OUTPUTS</span></span>

### <span data-ttu-id="56d9b-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="56d9b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="56d9b-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="56d9b-127">NOTES</span></span>

## <span data-ttu-id="56d9b-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56d9b-128">RELATED LINKS</span></span>

[<span data-ttu-id="56d9b-129">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="56d9b-129">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="56d9b-130">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="56d9b-130">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)
