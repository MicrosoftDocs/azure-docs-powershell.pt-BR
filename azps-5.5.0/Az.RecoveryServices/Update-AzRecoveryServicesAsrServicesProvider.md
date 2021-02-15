---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: ff280c11ff06d710eb8c74f88b839854506c6cd0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112677"
---
# <span data-ttu-id="8439d-101">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8439d-101">Update-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="8439d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8439d-102">SYNOPSIS</span></span>
<span data-ttu-id="8439d-103">Atualiza (Servidor de atualização) as informações recebidas do Provedor de Serviços de Recuperação de Sites do Azure.</span><span class="sxs-lookup"><span data-stu-id="8439d-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

## <span data-ttu-id="8439d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8439d-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8439d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8439d-105">DESCRIPTION</span></span>
<span data-ttu-id="8439d-106">O cmdlet **Update-AzRecoveryServicesAsrServicesProvider** atualiza as informações recebidas do Provedor de Serviços de Recuperação de Sites do Azure.</span><span class="sxs-lookup"><span data-stu-id="8439d-106">The **Update-AzRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="8439d-107">Você pode usar esse cmdlet para disparar uma atualização das informações recebidas do Provedor de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="8439d-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="8439d-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8439d-108">EXAMPLES</span></span>

### <span data-ttu-id="8439d-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8439d-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="8439d-110">Inicia a operação de atualização das informações do provedor de serviços ASR especificado e retorna o trabalho ASR usado para controlar a operação.</span><span class="sxs-lookup"><span data-stu-id="8439d-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8439d-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8439d-111">PARAMETERS</span></span>

### <span data-ttu-id="8439d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8439d-112">-DefaultProfile</span></span>
<span data-ttu-id="8439d-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8439d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8439d-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8439d-114">-InputObject</span></span>
<span data-ttu-id="8439d-115">Especifica o objeto do provedor de serviços ASR que identifica o servidor para o qual as informações serão atualizadas(atualizadas).)</span><span class="sxs-lookup"><span data-stu-id="8439d-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="8439d-116">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8439d-116">-Confirm</span></span>
<span data-ttu-id="8439d-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8439d-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8439d-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8439d-118">-WhatIf</span></span>
<span data-ttu-id="8439d-119">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8439d-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8439d-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8439d-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8439d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8439d-121">CommonParameters</span></span>
<span data-ttu-id="8439d-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8439d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8439d-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8439d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8439d-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="8439d-124">INPUTS</span></span>

### <span data-ttu-id="8439d-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8439d-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="8439d-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="8439d-126">OUTPUTS</span></span>

### <span data-ttu-id="8439d-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="8439d-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8439d-128">Notas</span><span class="sxs-lookup"><span data-stu-id="8439d-128">NOTES</span></span>

## <span data-ttu-id="8439d-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8439d-129">RELATED LINKS</span></span>

[<span data-ttu-id="8439d-130">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8439d-130">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="8439d-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8439d-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)
