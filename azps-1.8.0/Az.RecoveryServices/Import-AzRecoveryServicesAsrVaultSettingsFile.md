---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/import-azrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: 68ae9b9ad54772ba4157e02ebe602f35b2b5fe64
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399779"
---
# <span data-ttu-id="01893-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="01893-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="01893-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="01893-102">SYNOPSIS</span></span>
<span data-ttu-id="01893-103">Importa o arquivo de configurações do cofre ASR especificado para definir o contexto do cofre (contexto de sessão do PowerShell) para operações de ASR subsequentes na sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="01893-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

## <span data-ttu-id="01893-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01893-104">SYNTAX</span></span>

```
Import-AzRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01893-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="01893-105">DESCRIPTION</span></span>
<span data-ttu-id="01893-106">O cmdlet **Import-AzRecoveryServicesAsrVaultSettingsFile** importa o arquivo de configurações do cofre de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="01893-106">The **Import-AzRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="01893-107">O arquivo de configurações do cofre é usado para definir o contexto do cofre para as operações subsequentes de Recuperação de Site do Azure na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="01893-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="01893-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="01893-108">EXAMPLES</span></span>

### <span data-ttu-id="01893-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="01893-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="01893-110">Importa o arquivo de configurações do cofre dos Serviços de Recuperação especificado e retorna as configurações do cofre importado.</span><span class="sxs-lookup"><span data-stu-id="01893-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="01893-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01893-111">PARAMETERS</span></span>

### <span data-ttu-id="01893-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01893-112">-DefaultProfile</span></span>
<span data-ttu-id="01893-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="01893-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="01893-114">-Caminho</span><span class="sxs-lookup"><span data-stu-id="01893-114">-Path</span></span>
<span data-ttu-id="01893-115">Especifica o caminho da pasta do arquivo de configurações do cofre ASR.</span><span class="sxs-lookup"><span data-stu-id="01893-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="01893-116">Esse arquivo pode ser baixado do portal do cofre dos Serviços de Recuperação e armazenado localmente.</span><span class="sxs-lookup"><span data-stu-id="01893-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

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

### <span data-ttu-id="01893-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="01893-117">-Confirm</span></span>
<span data-ttu-id="01893-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01893-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01893-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01893-119">-WhatIf</span></span>
<span data-ttu-id="01893-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="01893-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01893-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="01893-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01893-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01893-122">CommonParameters</span></span>
<span data-ttu-id="01893-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01893-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01893-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01893-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01893-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="01893-125">INPUTS</span></span>

### <span data-ttu-id="01893-126">System.String</span><span class="sxs-lookup"><span data-stu-id="01893-126">System.String</span></span>

## <span data-ttu-id="01893-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="01893-127">OUTPUTS</span></span>

### <span data-ttu-id="01893-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="01893-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="01893-129">Notas</span><span class="sxs-lookup"><span data-stu-id="01893-129">NOTES</span></span>

## <span data-ttu-id="01893-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01893-130">RELATED LINKS</span></span>

