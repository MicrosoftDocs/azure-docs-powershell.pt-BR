---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/import-azrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: b287e69093ca748d02cd3f630e3b38fb51cdf8f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892611"
---
# <span data-ttu-id="c3e91-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="c3e91-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="c3e91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3e91-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e91-103">Importa o arquivo de configurações de cofre ASR especificado para definir o contexto do cofre (contexto de sessão do PowerShell) para operações ASR subsequentes na sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c3e91-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

## <span data-ttu-id="c3e91-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c3e91-104">SYNTAX</span></span>

```
Import-AzRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3e91-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c3e91-105">DESCRIPTION</span></span>
<span data-ttu-id="c3e91-106">O cmdlet **Import-AzRecoveryServicesAsrVaultSettingsFile** importa o arquivo de configurações do cofre de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="c3e91-106">The **Import-AzRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="c3e91-107">O arquivo de configurações do cofre é usado para definir o contexto do cofre para operações subsequentes de Recuperação de Site do Azure na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="c3e91-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="c3e91-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3e91-108">EXAMPLES</span></span>

### <span data-ttu-id="c3e91-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c3e91-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="c3e91-110">Importa o arquivo de configurações do cofre dos Serviços de Recuperação especificado e retorna as configurações do cofre importado.</span><span class="sxs-lookup"><span data-stu-id="c3e91-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="c3e91-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c3e91-111">PARAMETERS</span></span>

### <span data-ttu-id="c3e91-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e91-112">-DefaultProfile</span></span>
<span data-ttu-id="c3e91-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c3e91-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c3e91-114">-Path</span><span class="sxs-lookup"><span data-stu-id="c3e91-114">-Path</span></span>
<span data-ttu-id="c3e91-115">Especifica o caminho da pasta do arquivo de configurações do cofre ASR.</span><span class="sxs-lookup"><span data-stu-id="c3e91-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="c3e91-116">Esse arquivo pode ser baixado do portal do cofre dos Serviços de Recuperação e armazenado localmente.</span><span class="sxs-lookup"><span data-stu-id="c3e91-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

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

### <span data-ttu-id="c3e91-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3e91-117">-Confirm</span></span>
<span data-ttu-id="c3e91-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3e91-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3e91-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3e91-119">-WhatIf</span></span>
<span data-ttu-id="c3e91-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c3e91-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3e91-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c3e91-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3e91-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e91-122">CommonParameters</span></span>
<span data-ttu-id="c3e91-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3e91-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e91-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3e91-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e91-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c3e91-125">INPUTS</span></span>

### <span data-ttu-id="c3e91-126">System.String</span><span class="sxs-lookup"><span data-stu-id="c3e91-126">System.String</span></span>

## <span data-ttu-id="c3e91-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c3e91-127">OUTPUTS</span></span>

### <span data-ttu-id="c3e91-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="c3e91-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="c3e91-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="c3e91-129">NOTES</span></span>

## <span data-ttu-id="c3e91-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3e91-130">RELATED LINKS</span></span>

[<span data-ttu-id="c3e91-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="c3e91-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzRecoveryServicesAsrVaultSettingsFile.md)
