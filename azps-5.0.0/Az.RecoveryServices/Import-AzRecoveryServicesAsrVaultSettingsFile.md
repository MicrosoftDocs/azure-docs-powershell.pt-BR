---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/import-azrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: de3604a4bf1f9c46bf88b2f3cda25982672e9096
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116020"
---
# <span data-ttu-id="e714d-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="e714d-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="e714d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e714d-102">SYNOPSIS</span></span>
<span data-ttu-id="e714d-103">Importa o arquivo de configurações do cofre ASR especificado para definir o contexto do cofre (contexto da sessão do PowerShell) para operações ASR subsequentes na sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e714d-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

## <span data-ttu-id="e714d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e714d-104">SYNTAX</span></span>

```
Import-AzRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e714d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e714d-105">DESCRIPTION</span></span>
<span data-ttu-id="e714d-106">O cmdlet **Import-AzRecoveryServicesAsrVaultSettingsFile** importa o arquivo de configurações do cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e714d-106">The **Import-AzRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="e714d-107">O arquivo de configurações de cofre é usado para definir o contexto do cofre para operações subsequentes de recuperação de site do Azure na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="e714d-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="e714d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e714d-108">EXAMPLES</span></span>

### <span data-ttu-id="e714d-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e714d-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="e714d-110">Importa o arquivo de configurações do cofre de serviços de recuperação especificado e retorna as configurações do cofre importado.</span><span class="sxs-lookup"><span data-stu-id="e714d-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="e714d-111">OS</span><span class="sxs-lookup"><span data-stu-id="e714d-111">PARAMETERS</span></span>

### <span data-ttu-id="e714d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e714d-112">-DefaultProfile</span></span>
<span data-ttu-id="e714d-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e714d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e714d-114">-Caminho</span><span class="sxs-lookup"><span data-stu-id="e714d-114">-Path</span></span>
<span data-ttu-id="e714d-115">Especifica o caminho da pasta do arquivo de configurações do cofre ASR.</span><span class="sxs-lookup"><span data-stu-id="e714d-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="e714d-116">Esse arquivo pode ser baixado do portal de compartimento de serviços de recuperação e armazenado localmente.</span><span class="sxs-lookup"><span data-stu-id="e714d-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

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

### <span data-ttu-id="e714d-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e714d-117">-Confirm</span></span>
<span data-ttu-id="e714d-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e714d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e714d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e714d-119">-WhatIf</span></span>
<span data-ttu-id="e714d-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e714d-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e714d-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e714d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e714d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e714d-122">CommonParameters</span></span>
<span data-ttu-id="e714d-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e714d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e714d-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e714d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e714d-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e714d-125">INPUTS</span></span>

### <span data-ttu-id="e714d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e714d-126">System.String</span></span>

## <span data-ttu-id="e714d-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e714d-127">OUTPUTS</span></span>

### <span data-ttu-id="e714d-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="e714d-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="e714d-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e714d-129">NOTES</span></span>

## <span data-ttu-id="e714d-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e714d-130">RELATED LINKS</span></span>

[<span data-ttu-id="e714d-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="e714d-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzRecoveryServicesAsrVaultSettingsFile.md)
