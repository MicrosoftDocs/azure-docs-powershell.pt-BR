---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 9a9fbf8c25eba6206b3852476b5a72a2f96be423
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118031"
---
# <span data-ttu-id="f8bf5-101">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="f8bf5-101">Remove-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="f8bf5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f8bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="f8bf5-103">Exclui/cancela o registro do provedor de serviços de recuperação do Azure site Recovery especificado no cofre dos serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="f8bf5-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

## <span data-ttu-id="f8bf5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8bf5-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8bf5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f8bf5-105">DESCRIPTION</span></span>
<span data-ttu-id="f8bf5-106">O cmdlet **Remove-AzRecoveryServicesAsrServicesProvider** remove o provedor de serviços de recuperação do Azure site Recovery especificado do cofre.</span><span class="sxs-lookup"><span data-stu-id="f8bf5-106">The **Remove-AzRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="f8bf5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f8bf5-107">EXAMPLES</span></span>

### <span data-ttu-id="f8bf5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f8bf5-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="f8bf5-109">Inicia a exclusão/cancelamento de registro do provedor de serviços de recuperação de site do Azure especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="f8bf5-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f8bf5-110">OS</span><span class="sxs-lookup"><span data-stu-id="f8bf5-110">PARAMETERS</span></span>

### <span data-ttu-id="f8bf5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8bf5-111">-DefaultProfile</span></span>
<span data-ttu-id="f8bf5-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f8bf5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f8bf5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f8bf5-113">-Force</span></span>
<span data-ttu-id="f8bf5-114">Force o comando a ser executado sem fornecer um aviso adicional.</span><span class="sxs-lookup"><span data-stu-id="f8bf5-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="f8bf5-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8bf5-115">-InputObject</span></span>
<span data-ttu-id="f8bf5-116">O objeto de entrada para o cmdlet: o objeto do provedor de serviços de recuperação ASR correspondente ao provedor de serviços de recuperação ASR a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="f8bf5-116">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8bf5-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f8bf5-117">-Confirm</span></span>
<span data-ttu-id="f8bf5-118">Especifique se a confirmação é necessária.</span><span class="sxs-lookup"><span data-stu-id="f8bf5-118">Specify if confirmation is required.</span></span> <span data-ttu-id="f8bf5-119">Defina o valor do parâmetro Confirm para $false a fim de ignorar a confirmação.</span><span class="sxs-lookup"><span data-stu-id="f8bf5-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="f8bf5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8bf5-120">-WhatIf</span></span>
<span data-ttu-id="f8bf5-121">Mostra o que aconteceria se o cmdlet fosse executado sem realmente executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8bf5-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="f8bf5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8bf5-122">CommonParameters</span></span>
<span data-ttu-id="f8bf5-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8bf5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8bf5-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8bf5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8bf5-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f8bf5-125">INPUTS</span></span>

### <span data-ttu-id="f8bf5-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="f8bf5-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="f8bf5-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f8bf5-127">OUTPUTS</span></span>

### <span data-ttu-id="f8bf5-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f8bf5-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f8bf5-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f8bf5-129">NOTES</span></span>

## <span data-ttu-id="f8bf5-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8bf5-130">RELATED LINKS</span></span>

[<span data-ttu-id="f8bf5-131">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="f8bf5-131">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="f8bf5-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="f8bf5-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)
