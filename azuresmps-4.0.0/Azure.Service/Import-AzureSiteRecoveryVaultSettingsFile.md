---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 5875D72D-B8DB-4F72-BF5C-242D40A13DE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5dc0762021db2545b73a9ba7b9d7c53d435ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946260"
---
# <span data-ttu-id="e9b55-101">Import-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="e9b55-101">Import-AzureSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="e9b55-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9b55-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b55-103">Importa um arquivo de configurações do cofre de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="e9b55-103">Imports a Site Recovery vault settings file.</span></span>

## <span data-ttu-id="e9b55-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9b55-104">SYNTAX</span></span>

```
Import-AzureSiteRecoveryVaultSettingsFile -Path <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e9b55-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e9b55-105">DESCRIPTION</span></span>
<span data-ttu-id="e9b55-106">O cmdlet **Import-AzureSiteRecoveryVaultSettingsFile** importa um arquivo de configurações de cofre do Azure site Recovery para definir o contexto do cofre para operações subsequentes de recuperação de site na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="e9b55-106">The **Import-AzureSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="e9b55-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9b55-107">EXAMPLES</span></span>

### <span data-ttu-id="e9b55-108">Exemplo 1: importar um arquivo de configurações de cofre</span><span class="sxs-lookup"><span data-stu-id="e9b55-108">Example 1: Import a vault settings file</span></span>
```
PS C:\> Import-AzureSiteRecoveryVaultSettingsFile -Path "C:\Users\Contoso\Contosovault Monday, October 6, 2014.VaultCredentials"
VERBOSE: Vault Settings File path: C:\Users\Contoso\Contosovault Monday, October 6, 2014.VaultCredentials

ResourceName                                                CloudServiceName
------------                                                ----------------
Contosovault                                                RecoveryServices-6JP23WE3SKKOM5AFQG2YQAI22MNOWK52QDKWMUP...
```

<span data-ttu-id="e9b55-109">Este comando importa o arquivo de configurações do cofre no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="e9b55-109">This command imports the vault settings file at the specified path.</span></span>

## <span data-ttu-id="e9b55-110">OS</span><span class="sxs-lookup"><span data-stu-id="e9b55-110">PARAMETERS</span></span>

### <span data-ttu-id="e9b55-111">-Caminho</span><span class="sxs-lookup"><span data-stu-id="e9b55-111">-Path</span></span>
<span data-ttu-id="e9b55-112">Especifica o caminho do arquivo de configurações do cofre de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="e9b55-112">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="e9b55-113">Esse arquivo pode ser baixado do portal de cofre do site Recovery e armazenado localmente.</span><span class="sxs-lookup"><span data-stu-id="e9b55-113">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9b55-114">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e9b55-114">-Profile</span></span>
<span data-ttu-id="e9b55-115">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e9b55-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e9b55-116">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e9b55-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b55-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b55-117">CommonParameters</span></span>
<span data-ttu-id="e9b55-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9b55-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b55-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9b55-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b55-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e9b55-120">INPUTS</span></span>

## <span data-ttu-id="e9b55-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e9b55-121">OUTPUTS</span></span>

## <span data-ttu-id="e9b55-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e9b55-122">NOTES</span></span>

## <span data-ttu-id="e9b55-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9b55-123">RELATED LINKS</span></span>

[<span data-ttu-id="e9b55-124">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="e9b55-124">Get-AzureSiteRecoveryVaultSettings</span></span>](./Get-AzureSiteRecoveryVaultSettings.md)

[<span data-ttu-id="e9b55-125">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="e9b55-125">Get-AzureSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureSiteRecoveryVaultSettingsFile.md)


