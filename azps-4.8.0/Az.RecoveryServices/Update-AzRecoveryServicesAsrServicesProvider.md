---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: ff280c11ff06d710eb8c74f88b839854506c6cd0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114240"
---
# <span data-ttu-id="85bc0-101">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="85bc0-101">Update-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="85bc0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="85bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="85bc0-103">Atualiza (atualizar servidor) as informações recebidas do provedor de serviços de recuperação do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="85bc0-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

## <span data-ttu-id="85bc0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85bc0-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85bc0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="85bc0-105">DESCRIPTION</span></span>
<span data-ttu-id="85bc0-106">O cmdlet **Update-AzRecoveryServicesAsrServicesProvider** atualiza as informações recebidas do provedor de serviços de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="85bc0-106">The **Update-AzRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="85bc0-107">Você pode usar esse cmdlet para disparar uma atualização das informações recebidas do provedor de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="85bc0-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="85bc0-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="85bc0-108">EXAMPLES</span></span>

### <span data-ttu-id="85bc0-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="85bc0-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="85bc0-110">Inicia a operação de atualização das informações do provedor de serviços ASR especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="85bc0-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="85bc0-111">OS</span><span class="sxs-lookup"><span data-stu-id="85bc0-111">PARAMETERS</span></span>

### <span data-ttu-id="85bc0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85bc0-112">-DefaultProfile</span></span>
<span data-ttu-id="85bc0-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="85bc0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="85bc0-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85bc0-114">-InputObject</span></span>
<span data-ttu-id="85bc0-115">Especifica o objeto do provedor de serviços ASR que identifica o servidor para o qual as informações serão atualizadas (atualizado.)</span><span class="sxs-lookup"><span data-stu-id="85bc0-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="85bc0-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="85bc0-116">-Confirm</span></span>
<span data-ttu-id="85bc0-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85bc0-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85bc0-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85bc0-118">-WhatIf</span></span>
<span data-ttu-id="85bc0-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="85bc0-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85bc0-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="85bc0-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85bc0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85bc0-121">CommonParameters</span></span>
<span data-ttu-id="85bc0-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85bc0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85bc0-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85bc0-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85bc0-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="85bc0-124">INPUTS</span></span>

### <span data-ttu-id="85bc0-125">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="85bc0-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="85bc0-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="85bc0-126">OUTPUTS</span></span>

### <span data-ttu-id="85bc0-127">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="85bc0-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="85bc0-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="85bc0-128">NOTES</span></span>

## <span data-ttu-id="85bc0-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85bc0-129">RELATED LINKS</span></span>

[<span data-ttu-id="85bc0-130">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="85bc0-130">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="85bc0-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="85bc0-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)
