---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 823ad4b0f7eff8f80fea012bdef4b3c2662d55e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427457"
---
# <span data-ttu-id="798af-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="798af-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="798af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="798af-102">SYNOPSIS</span></span>
<span data-ttu-id="798af-103">Atualiza (atualizar servidor) as informações recebidas do provedor de serviços de recuperação do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="798af-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="798af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="798af-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="798af-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="798af-105">DESCRIPTION</span></span>
<span data-ttu-id="798af-106">O cmdlet **Update-AzureRmRecoveryServicesAsrServicesProvider** atualiza as informações recebidas do provedor de serviços de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="798af-106">The **Update-AzureRmRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="798af-107">Você pode usar esse cmdlet para disparar uma atualização das informações recebidas do provedor de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="798af-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="798af-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="798af-108">EXAMPLES</span></span>

### <span data-ttu-id="798af-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="798af-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="798af-110">Inicia a operação de atualização das informações do provedor de serviços ASR especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="798af-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="798af-111">OS</span><span class="sxs-lookup"><span data-stu-id="798af-111">PARAMETERS</span></span>

### <span data-ttu-id="798af-112">-Confirme</span><span class="sxs-lookup"><span data-stu-id="798af-112">-Confirm</span></span>
<span data-ttu-id="798af-113">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="798af-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="798af-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="798af-114">-DefaultProfile</span></span>
<span data-ttu-id="798af-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="798af-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="798af-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="798af-116">-InputObject</span></span>
<span data-ttu-id="798af-117">Especifica o objeto do provedor de serviços ASR que identifica o servidor para o qual as informações serão atualizadas (atualizado.)</span><span class="sxs-lookup"><span data-stu-id="798af-117">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="798af-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="798af-118">-WhatIf</span></span>
<span data-ttu-id="798af-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="798af-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="798af-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="798af-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="798af-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="798af-121">CommonParameters</span></span>
<span data-ttu-id="798af-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="798af-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="798af-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="798af-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="798af-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="798af-124">INPUTS</span></span>

### <span data-ttu-id="798af-125">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="798af-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="798af-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="798af-126">OUTPUTS</span></span>

### <span data-ttu-id="798af-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="798af-127">System.Object</span></span>

## <span data-ttu-id="798af-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="798af-128">NOTES</span></span>

## <span data-ttu-id="798af-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="798af-129">RELATED LINKS</span></span>

[<span data-ttu-id="798af-130">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="798af-130">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="798af-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="798af-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)
