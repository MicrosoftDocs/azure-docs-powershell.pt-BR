---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 25475bd87579b693555280f3c465f157d69c807a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948073"
---
# <span data-ttu-id="8e72c-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="8e72c-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="8e72c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e72c-102">SYNOPSIS</span></span>
<span data-ttu-id="8e72c-103">Exclui o mapeamento de contêiner da proteção do Azure site Recovery especificado.</span><span class="sxs-lookup"><span data-stu-id="8e72c-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="8e72c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e72c-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e72c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8e72c-105">DESCRIPTION</span></span>
<span data-ttu-id="8e72c-106">O cmdlet **Remove-AzRecoveryServicesAsrProtectionContainerMapping** exclui o mapeamento de contêiner da proteção do Azure site Recovery especificado.</span><span class="sxs-lookup"><span data-stu-id="8e72c-106">The **Remove-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="8e72c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e72c-107">EXAMPLES</span></span>

### <span data-ttu-id="8e72c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8e72c-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="8e72c-109">Inicia a exclusão do mapeamento de contêiner de proteção especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="8e72c-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8e72c-110">OS</span><span class="sxs-lookup"><span data-stu-id="8e72c-110">PARAMETERS</span></span>

### <span data-ttu-id="8e72c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e72c-111">-DefaultProfile</span></span>
<span data-ttu-id="8e72c-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e72c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8e72c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8e72c-113">-Force</span></span>
<span data-ttu-id="8e72c-114">Force o comando a ser executado sem fornecer um aviso adicional.</span><span class="sxs-lookup"><span data-stu-id="8e72c-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="8e72c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e72c-115">-InputObject</span></span>
<span data-ttu-id="8e72c-116">O objeto de entrada para o cmdlet: o objeto de mapeamento do contêiner de proteção ASR correspondente ao contêiner de proteção a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="8e72c-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

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

### <span data-ttu-id="8e72c-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8e72c-117">-Confirm</span></span>
<span data-ttu-id="8e72c-118">Especifique se a confirmação é necessária.</span><span class="sxs-lookup"><span data-stu-id="8e72c-118">Specify if confirmation is required.</span></span> <span data-ttu-id="8e72c-119">Defina o valor do parâmetro Confirm para $false a fim de ignorar a confirmação</span><span class="sxs-lookup"><span data-stu-id="8e72c-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="8e72c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e72c-120">-WhatIf</span></span>
<span data-ttu-id="8e72c-121">Mostra o que aconteceria se o cmdlet fosse executado sem realmente executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e72c-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="8e72c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e72c-122">CommonParameters</span></span>
<span data-ttu-id="8e72c-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e72c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e72c-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e72c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e72c-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8e72c-125">INPUTS</span></span>

### <span data-ttu-id="8e72c-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="8e72c-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="8e72c-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8e72c-127">OUTPUTS</span></span>

### <span data-ttu-id="8e72c-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8e72c-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8e72c-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8e72c-129">NOTES</span></span>

## <span data-ttu-id="8e72c-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e72c-130">RELATED LINKS</span></span>

[<span data-ttu-id="8e72c-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="8e72c-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="8e72c-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="8e72c-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)
