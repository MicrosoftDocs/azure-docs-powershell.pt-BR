---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: f034f91f026538bbae475466fbd9d3afa7067145
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440303"
---
# <span data-ttu-id="5060c-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5060c-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="5060c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5060c-102">SYNOPSIS</span></span>
<span data-ttu-id="5060c-103">Exclui o mapeamento de contêiner da proteção do Azure site Recovery especificado.</span><span class="sxs-lookup"><span data-stu-id="5060c-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5060c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5060c-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5060c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5060c-105">DESCRIPTION</span></span>
<span data-ttu-id="5060c-106">O cmdlet **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** exclui o mapeamento de contêiner da proteção do Azure site Recovery especificado.</span><span class="sxs-lookup"><span data-stu-id="5060c-106">The **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="5060c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5060c-107">EXAMPLES</span></span>

### <span data-ttu-id="5060c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5060c-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="5060c-109">Inicia a exclusão do mapeamento de contêiner de proteção especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="5060c-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5060c-110">OS</span><span class="sxs-lookup"><span data-stu-id="5060c-110">PARAMETERS</span></span>

### <span data-ttu-id="5060c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5060c-111">-DefaultProfile</span></span>
<span data-ttu-id="5060c-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5060c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="5060c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5060c-113">-Force</span></span>
<span data-ttu-id="5060c-114">Force o comando a ser executado sem fornecer um aviso adicional.</span><span class="sxs-lookup"><span data-stu-id="5060c-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="5060c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5060c-115">-InputObject</span></span>
<span data-ttu-id="5060c-116">O objeto de entrada para o cmdlet: o objeto de mapeamento do contêiner de proteção ASR correspondente ao contêiner de proteção a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="5060c-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5060c-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5060c-117">-Confirm</span></span>
<span data-ttu-id="5060c-118">Especifique se a confirmação é necessária.</span><span class="sxs-lookup"><span data-stu-id="5060c-118">Specify if confirmation is required.</span></span> <span data-ttu-id="5060c-119">Defina o valor do parâmetro Confirm para $false a fim de ignorar a confirmação</span><span class="sxs-lookup"><span data-stu-id="5060c-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="5060c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5060c-120">-WhatIf</span></span>
<span data-ttu-id="5060c-121">Mostra o que aconteceria se o cmdlet fosse executado sem realmente executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5060c-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="5060c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5060c-122">CommonParameters</span></span>
<span data-ttu-id="5060c-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5060c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5060c-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5060c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5060c-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5060c-125">INPUTS</span></span>

### <span data-ttu-id="5060c-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5060c-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="5060c-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5060c-127">OUTPUTS</span></span>

### <span data-ttu-id="5060c-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5060c-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5060c-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5060c-129">NOTES</span></span>

## <span data-ttu-id="5060c-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5060c-130">RELATED LINKS</span></span>

[<span data-ttu-id="5060c-131">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5060c-131">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="5060c-132">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5060c-132">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
