---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: ef251bb9d1060e511658f9174cde2c04ab288ed7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114036"
---
# <span data-ttu-id="2c24a-101">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="2c24a-101">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="2c24a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c24a-102">SYNOPSIS</span></span>
<span data-ttu-id="2c24a-103">Exclui o mapeamento de rede ASR especificado do cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="2c24a-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

## <span data-ttu-id="2c24a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c24a-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c24a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2c24a-105">DESCRIPTION</span></span>
<span data-ttu-id="2c24a-106">O cmdlet **Remove-AzRecoveryServicesAsrNetWorkMapping** exclui o mapeamento de rede ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="2c24a-106">The **Remove-AzRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="2c24a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2c24a-107">EXAMPLES</span></span>

### <span data-ttu-id="2c24a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2c24a-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="2c24a-109">Inicia a exclusão do mapeamento de rede ASR especificado e retorna o trabalho ASR usado para controlar a operação.</span><span class="sxs-lookup"><span data-stu-id="2c24a-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="2c24a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c24a-110">PARAMETERS</span></span>

### <span data-ttu-id="2c24a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c24a-111">-DefaultProfile</span></span>
<span data-ttu-id="2c24a-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c24a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2c24a-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c24a-113">-InputObject</span></span>
<span data-ttu-id="2c24a-114">O objeto de entrada para o cmdlet: o objeto de mapeamento de rede ASR correspondente ao mapeamento de rede ASR a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="2c24a-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

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

### <span data-ttu-id="2c24a-115">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2c24a-115">-Confirm</span></span>
<span data-ttu-id="2c24a-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c24a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c24a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c24a-117">-WhatIf</span></span>
<span data-ttu-id="2c24a-118">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2c24a-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c24a-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c24a-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c24a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c24a-120">CommonParameters</span></span>
<span data-ttu-id="2c24a-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c24a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c24a-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c24a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c24a-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="2c24a-123">INPUTS</span></span>

### <span data-ttu-id="2c24a-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="2c24a-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="2c24a-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="2c24a-125">OUTPUTS</span></span>

### <span data-ttu-id="2c24a-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="2c24a-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2c24a-127">Notas</span><span class="sxs-lookup"><span data-stu-id="2c24a-127">NOTES</span></span>

## <span data-ttu-id="2c24a-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c24a-128">RELATED LINKS</span></span>

[<span data-ttu-id="2c24a-129">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="2c24a-129">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="2c24a-130">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="2c24a-130">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)
