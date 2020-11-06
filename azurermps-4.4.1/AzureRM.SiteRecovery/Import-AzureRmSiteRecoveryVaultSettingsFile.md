---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 070DA86E-9EA4-4777-9D53-64B58B4401B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 42863e0dbf6982ced1f77f916c97ed4fc19d6979
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440550"
---
# <span data-ttu-id="f3ff0-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f3ff0-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="f3ff0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f3ff0-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ff0-103">Importa um arquivo de configurações do cofre de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="f3ff0-103">Imports a Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3ff0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3ff0-104">SYNTAX</span></span>

```
Import-AzureRmSiteRecoveryVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3ff0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f3ff0-105">DESCRIPTION</span></span>
<span data-ttu-id="f3ff0-106">O cmdlet **Import-AzureRmSiteRecoveryVaultSettingsFile** importa um arquivo de configurações de cofre do Azure site Recovery para definir o contexto do cofre para operações subsequentes de recuperação de site na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="f3ff0-106">The **Import-AzureRmSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="f3ff0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f3ff0-107">EXAMPLES</span></span>

## <span data-ttu-id="f3ff0-108">OS</span><span class="sxs-lookup"><span data-stu-id="f3ff0-108">PARAMETERS</span></span>

### <span data-ttu-id="f3ff0-109">-Caminho</span><span class="sxs-lookup"><span data-stu-id="f3ff0-109">-Path</span></span>
<span data-ttu-id="f3ff0-110">Especifica o caminho do arquivo de configurações do cofre de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="f3ff0-110">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="f3ff0-111">Esse arquivo pode ser baixado do portal de cofre do site Recovery e armazenado localmente.</span><span class="sxs-lookup"><span data-stu-id="f3ff0-111">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ff0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ff0-112">-DefaultProfile</span></span>
<span data-ttu-id="f3ff0-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f3ff0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3ff0-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ff0-114">CommonParameters</span></span>
<span data-ttu-id="f3ff0-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3ff0-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ff0-116">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3ff0-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ff0-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f3ff0-117">INPUTS</span></span>

## <span data-ttu-id="f3ff0-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f3ff0-118">OUTPUTS</span></span>

### <span data-ttu-id="f3ff0-119">Microsoft. Azure. Commands. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="f3ff0-119">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="f3ff0-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f3ff0-120">NOTES</span></span>

## <span data-ttu-id="f3ff0-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f3ff0-121">RELATED LINKS</span></span>

[<span data-ttu-id="f3ff0-122">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f3ff0-122">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureRmSiteRecoveryVaultSettingsFile.md)
