---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 60bcdad644f07f627373c90791c8cd115d590bcd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772946"
---
# <span data-ttu-id="e836e-101">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e836e-101">Update-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="e836e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e836e-102">SYNOPSIS</span></span>
<span data-ttu-id="e836e-103">Atualiza (atualizar servidor) as informações recebidas do provedor de serviços de recuperação do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="e836e-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

## <span data-ttu-id="e836e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e836e-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e836e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e836e-105">DESCRIPTION</span></span>
<span data-ttu-id="e836e-106">O cmdlet **Update-AzRecoveryServicesAsrServicesProvider** atualiza as informações recebidas do provedor de serviços de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="e836e-106">The **Update-AzRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="e836e-107">Você pode usar esse cmdlet para disparar uma atualização das informações recebidas do provedor de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="e836e-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="e836e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e836e-108">EXAMPLES</span></span>

### <span data-ttu-id="e836e-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e836e-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="e836e-110">Inicia a operação de atualização das informações do provedor de serviços ASR especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="e836e-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e836e-111">OS</span><span class="sxs-lookup"><span data-stu-id="e836e-111">PARAMETERS</span></span>

### <span data-ttu-id="e836e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e836e-112">-DefaultProfile</span></span>
<span data-ttu-id="e836e-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e836e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e836e-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e836e-114">-InputObject</span></span>
<span data-ttu-id="e836e-115">Especifica o objeto do provedor de serviços ASR que identifica o servidor para o qual as informações serão atualizadas (atualizado.)</span><span class="sxs-lookup"><span data-stu-id="e836e-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="e836e-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e836e-116">-Confirm</span></span>
<span data-ttu-id="e836e-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e836e-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e836e-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e836e-118">-WhatIf</span></span>
<span data-ttu-id="e836e-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e836e-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e836e-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e836e-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e836e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e836e-121">CommonParameters</span></span>
<span data-ttu-id="e836e-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e836e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e836e-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e836e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e836e-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e836e-124">INPUTS</span></span>

### <span data-ttu-id="e836e-125">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e836e-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="e836e-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e836e-126">OUTPUTS</span></span>

### <span data-ttu-id="e836e-127">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e836e-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e836e-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e836e-128">NOTES</span></span>

## <span data-ttu-id="e836e-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e836e-129">RELATED LINKS</span></span>

[<span data-ttu-id="e836e-130">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e836e-130">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="e836e-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e836e-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)
