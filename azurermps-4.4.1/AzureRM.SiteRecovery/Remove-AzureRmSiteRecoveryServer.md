---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3302054E-C5BB-4B89-B9C9-ED7572DFA234
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: 4be04d590adbf75760472f4047b7de9efcffd2d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610710"
---
# <span data-ttu-id="2107a-101">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="2107a-101">Remove-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="2107a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2107a-102">SYNOPSIS</span></span>
<span data-ttu-id="2107a-103">Remove um servidor de recuperação de site do cofre atual.</span><span class="sxs-lookup"><span data-stu-id="2107a-103">Removes a Site Recovery server from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2107a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2107a-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServer -Server <ASRServer> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2107a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2107a-105">DESCRIPTION</span></span>
<span data-ttu-id="2107a-106">O cmdlet **Remove-AzureRmSiteRecoveryServer** cancela o registro de um servidor de recuperação de site do Azure que o Remove do cofre atual.</span><span class="sxs-lookup"><span data-stu-id="2107a-106">The **Remove-AzureRmSiteRecoveryServer** cmdlet unregisters an Azure Site Recovery server which removes it from the current vault.</span></span>

## <span data-ttu-id="2107a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2107a-107">EXAMPLES</span></span>

## <span data-ttu-id="2107a-108">OS</span><span class="sxs-lookup"><span data-stu-id="2107a-108">PARAMETERS</span></span>

### <span data-ttu-id="2107a-109">-Force</span><span class="sxs-lookup"><span data-stu-id="2107a-109">-Force</span></span>
<span data-ttu-id="2107a-110">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="2107a-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2107a-111">-Servidor</span><span class="sxs-lookup"><span data-stu-id="2107a-111">-Server</span></span>
<span data-ttu-id="2107a-112">Especifica o objeto do servidor de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="2107a-112">Specifies the Site Recovery server object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2107a-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2107a-113">-Confirm</span></span>
<span data-ttu-id="2107a-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2107a-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2107a-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2107a-115">-WhatIf</span></span>
<span data-ttu-id="2107a-116">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2107a-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="2107a-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2107a-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2107a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2107a-118">-DefaultProfile</span></span>
<span data-ttu-id="2107a-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2107a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2107a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2107a-120">CommonParameters</span></span>
<span data-ttu-id="2107a-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2107a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2107a-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2107a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2107a-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2107a-123">INPUTS</span></span>

### <span data-ttu-id="2107a-124">ASRServer</span><span class="sxs-lookup"><span data-stu-id="2107a-124">ASRServer</span></span>
<span data-ttu-id="2107a-125">O parâmetro ' Server ' aceita o valor do tipo ' ASRServer ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="2107a-125">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="2107a-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2107a-126">OUTPUTS</span></span>

### <span data-ttu-id="2107a-127">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="2107a-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="2107a-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2107a-128">NOTES</span></span>

## <span data-ttu-id="2107a-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2107a-129">RELATED LINKS</span></span>

[<span data-ttu-id="2107a-130">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="2107a-130">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="2107a-131">Update-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="2107a-131">Update-AzureRmSiteRecoveryServer</span></span>](./Update-AzureRmSiteRecoveryServer.md)
