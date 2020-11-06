---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: ad22cbe1cb17e69358ef386b478fe929abe415b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602425"
---
# <span data-ttu-id="a562f-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="a562f-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="a562f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a562f-102">SYNOPSIS</span></span>
<span data-ttu-id="a562f-103">Importa o arquivo de configurações do cofre ASR especificado para definir o contexto do cofre (contexto da sessão do PowerShell) para operações ASR subsequentes na sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a562f-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a562f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a562f-104">SYNTAX</span></span>

```
Import-AzureRmRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a562f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a562f-105">DESCRIPTION</span></span>
<span data-ttu-id="a562f-106">O cmdlet **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** importa o arquivo de configurações do cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a562f-106">The **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="a562f-107">O arquivo de configurações de cofre é usado para definir o contexto do cofre para operações subsequentes de recuperação de site do Azure na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="a562f-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="a562f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a562f-108">EXAMPLES</span></span>

### <span data-ttu-id="a562f-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a562f-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzureRmRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="a562f-110">Importa o arquivo de configurações do cofre de serviços de recuperação especificado e retorna as configurações do cofre importado.</span><span class="sxs-lookup"><span data-stu-id="a562f-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="a562f-111">OS</span><span class="sxs-lookup"><span data-stu-id="a562f-111">PARAMETERS</span></span>

### <span data-ttu-id="a562f-112">-Caminho</span><span class="sxs-lookup"><span data-stu-id="a562f-112">-Path</span></span>
<span data-ttu-id="a562f-113">Especifica o caminho do arquivo de configurações do cofre ASR.</span><span class="sxs-lookup"><span data-stu-id="a562f-113">Specifies the path of the ASR vault settings file.</span></span>
<span data-ttu-id="a562f-114">Esse arquivo pode ser baixado do portal de compartimento de serviços de recuperação e armazenado localmente.</span><span class="sxs-lookup"><span data-stu-id="a562f-114">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a562f-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a562f-115">-Confirm</span></span>
<span data-ttu-id="a562f-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a562f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a562f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a562f-117">-WhatIf</span></span>
<span data-ttu-id="a562f-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a562f-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a562f-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a562f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a562f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a562f-120">CommonParameters</span></span>
<span data-ttu-id="a562f-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a562f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a562f-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a562f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a562f-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a562f-123">INPUTS</span></span>

### <span data-ttu-id="a562f-124">System. String</span><span class="sxs-lookup"><span data-stu-id="a562f-124">System.String</span></span>

## <span data-ttu-id="a562f-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a562f-125">OUTPUTS</span></span>

### <span data-ttu-id="a562f-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="a562f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="a562f-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a562f-127">NOTES</span></span>

## <span data-ttu-id="a562f-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a562f-128">RELATED LINKS</span></span>

[<span data-ttu-id="a562f-129">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="a562f-129">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesAsrVaultSettingsFile.md)
