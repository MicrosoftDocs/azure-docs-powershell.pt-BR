---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: f7d71d0e69f83633d02832bd3f54554be1fa0ba0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885542"
---
# <span data-ttu-id="3a71a-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3a71a-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="3a71a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a71a-102">SYNOPSIS</span></span>
<span data-ttu-id="3a71a-103">Exclui o mapeamento de contêineres de proteção de site do Azure Especificado.</span><span class="sxs-lookup"><span data-stu-id="3a71a-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="3a71a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3a71a-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a71a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3a71a-105">DESCRIPTION</span></span>
<span data-ttu-id="3a71a-106">O cmdlet **Remove-AzRecoveryServicesAsrProtectionContainerMapping** exclui o mapeamento especificado do contêiner de proteção de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="3a71a-106">The **Remove-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="3a71a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a71a-107">EXAMPLES</span></span>

### <span data-ttu-id="3a71a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3a71a-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="3a71a-109">Inicia a exclusão do mapeamento de contêineres de proteção especificado e retorna o trabalho ASR usado para rastrear a operação.</span><span class="sxs-lookup"><span data-stu-id="3a71a-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="3a71a-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3a71a-110">PARAMETERS</span></span>

### <span data-ttu-id="3a71a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a71a-111">-DefaultProfile</span></span>
<span data-ttu-id="3a71a-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a71a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="3a71a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3a71a-113">-Force</span></span>
<span data-ttu-id="3a71a-114">Force o comando a ser executado sem fornecer um aviso adicional.</span><span class="sxs-lookup"><span data-stu-id="3a71a-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="3a71a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a71a-115">-InputObject</span></span>
<span data-ttu-id="3a71a-116">O objeto de entrada do cmdlet: o objeto de mapeamento de contêiner de proteção ASR correspondente ao contêiner de proteção a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="3a71a-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

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

### <span data-ttu-id="3a71a-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a71a-117">-Confirm</span></span>
<span data-ttu-id="3a71a-118">Especifique se a confirmação é necessária.</span><span class="sxs-lookup"><span data-stu-id="3a71a-118">Specify if confirmation is required.</span></span> <span data-ttu-id="3a71a-119">Definir o valor do parâmetro confirme como $false para ignorar a confirmação</span><span class="sxs-lookup"><span data-stu-id="3a71a-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="3a71a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a71a-120">-WhatIf</span></span>
<span data-ttu-id="3a71a-121">Mostra o que aconteceria se o cmdlet fosse executado sem realmente executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a71a-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="3a71a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a71a-122">CommonParameters</span></span>
<span data-ttu-id="3a71a-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a71a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a71a-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a71a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a71a-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a71a-125">INPUTS</span></span>

### <span data-ttu-id="3a71a-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3a71a-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="3a71a-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3a71a-127">OUTPUTS</span></span>

### <span data-ttu-id="3a71a-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="3a71a-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3a71a-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="3a71a-129">NOTES</span></span>

## <span data-ttu-id="3a71a-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a71a-130">RELATED LINKS</span></span>

[<span data-ttu-id="3a71a-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3a71a-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="3a71a-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3a71a-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)
