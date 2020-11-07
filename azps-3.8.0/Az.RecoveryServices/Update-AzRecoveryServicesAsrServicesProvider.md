---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: ff280c11ff06d710eb8c74f88b839854506c6cd0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943513"
---
# <span data-ttu-id="ec0f9-101">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ec0f9-101">Update-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="ec0f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ec0f9-102">SYNOPSIS</span></span>
<span data-ttu-id="ec0f9-103">Atualiza (atualizar servidor) as informações recebidas do provedor de serviços de recuperação do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="ec0f9-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

## <span data-ttu-id="ec0f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec0f9-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec0f9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ec0f9-105">DESCRIPTION</span></span>
<span data-ttu-id="ec0f9-106">O cmdlet **Update-AzRecoveryServicesAsrServicesProvider** atualiza as informações recebidas do provedor de serviços de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="ec0f9-106">The **Update-AzRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="ec0f9-107">Você pode usar esse cmdlet para disparar uma atualização das informações recebidas do provedor de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="ec0f9-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="ec0f9-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ec0f9-108">EXAMPLES</span></span>

### <span data-ttu-id="ec0f9-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ec0f9-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="ec0f9-110">Inicia a operação de atualização das informações do provedor de serviços ASR especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="ec0f9-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ec0f9-111">OS</span><span class="sxs-lookup"><span data-stu-id="ec0f9-111">PARAMETERS</span></span>

### <span data-ttu-id="ec0f9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec0f9-112">-DefaultProfile</span></span>
<span data-ttu-id="ec0f9-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ec0f9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ec0f9-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec0f9-114">-InputObject</span></span>
<span data-ttu-id="ec0f9-115">Especifica o objeto do provedor de serviços ASR que identifica o servidor para o qual as informações serão atualizadas (atualizado.)</span><span class="sxs-lookup"><span data-stu-id="ec0f9-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="ec0f9-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ec0f9-116">-Confirm</span></span>
<span data-ttu-id="ec0f9-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec0f9-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec0f9-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec0f9-118">-WhatIf</span></span>
<span data-ttu-id="ec0f9-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ec0f9-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec0f9-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ec0f9-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec0f9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec0f9-121">CommonParameters</span></span>
<span data-ttu-id="ec0f9-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec0f9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec0f9-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec0f9-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec0f9-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ec0f9-124">INPUTS</span></span>

### <span data-ttu-id="ec0f9-125">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ec0f9-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="ec0f9-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ec0f9-126">OUTPUTS</span></span>

### <span data-ttu-id="ec0f9-127">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ec0f9-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ec0f9-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ec0f9-128">NOTES</span></span>

## <span data-ttu-id="ec0f9-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec0f9-129">RELATED LINKS</span></span>

[<span data-ttu-id="ec0f9-130">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ec0f9-130">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="ec0f9-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ec0f9-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)
