---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 70ADAF16-BC52-47BF-A85A-A84DEACDA027
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2704dbdc308b9773452b05ceba24719f2e274132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945676"
---
# <span data-ttu-id="b18fb-101">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="b18fb-101">Get-AzureAccount</span></span>

## <span data-ttu-id="b18fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b18fb-102">SYNOPSIS</span></span>
<span data-ttu-id="b18fb-103">Obtém contas do Azure que estão disponíveis para o PowerShell do Azure.</span><span class="sxs-lookup"><span data-stu-id="b18fb-103">Gets Azure accounts that are available to Azure PowerShell.</span></span>

## <span data-ttu-id="b18fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b18fb-104">SYNTAX</span></span>

```
Get-AzureAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b18fb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b18fb-105">DESCRIPTION</span></span>
<span data-ttu-id="b18fb-106">O cmdlet **Get-AzureAccount** Obtém as contas do Azure que estão disponíveis para o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b18fb-106">The **Get-AzureAccount** cmdlet gets the Azure accounts that are available to Windows PowerShell.</span></span>
<span data-ttu-id="b18fb-107">Para disponibilizar suas contas para o Windows PowerShell, use os cmdlets **Add-AzureAccount** ou **Import-PublishSettingsFile** .</span><span class="sxs-lookup"><span data-stu-id="b18fb-107">To make your accounts available to Windows PowerShell, use the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlets.</span></span>

## <span data-ttu-id="b18fb-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b18fb-108">EXAMPLES</span></span>

### <span data-ttu-id="b18fb-109">Exemplo 1: obter todas as contas</span><span class="sxs-lookup"><span data-stu-id="b18fb-109">Example 1: Get all accounts</span></span>
```
PS C:\> Get-AzureAccount

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
contosotest1@outlook.com     {{ ActiveDirectoryTenantId = aaeabcde-386c-4466-bf70-794...
```

<span data-ttu-id="b18fb-110">Esse comando obtém todas as contas associadas ao usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="b18fb-110">This command gets all accounts associated with the specified user.</span></span>

### <span data-ttu-id="b18fb-111">Exemplo 2: obter uma conta por nome</span><span class="sxs-lookup"><span data-stu-id="b18fb-111">Example 2: Get an account by name</span></span>
```
PS C:\> Get-AzureAccount -Name contosoadmin@outlook.com

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
```

<span data-ttu-id="b18fb-112">Esse comando obtém a conta ContosoAdmin.</span><span class="sxs-lookup"><span data-stu-id="b18fb-112">This command gets the ContosoAdmin account.</span></span>

## <span data-ttu-id="b18fb-113">OS</span><span class="sxs-lookup"><span data-stu-id="b18fb-113">PARAMETERS</span></span>

### <span data-ttu-id="b18fb-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="b18fb-114">-Name</span></span>
<span data-ttu-id="b18fb-115">Obtém apenas a conta especificada.</span><span class="sxs-lookup"><span data-stu-id="b18fb-115">Gets only the specified account.</span></span>
<span data-ttu-id="b18fb-116">O padrão é todas as contas que estão disponíveis para o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b18fb-116">The default is all accounts that are available to Windows PowerShell.</span></span>
<span data-ttu-id="b18fb-117">Digite o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="b18fb-117">Enter the account name.</span></span>
<span data-ttu-id="b18fb-118">O valor do **nome** diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b18fb-118">The **Name** value is case-sensitive.</span></span>
<span data-ttu-id="b18fb-119">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="b18fb-119">Wildcards are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18fb-120">-Perfil</span><span class="sxs-lookup"><span data-stu-id="b18fb-120">-Profile</span></span>
<span data-ttu-id="b18fb-121">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="b18fb-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="b18fb-122">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="b18fb-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b18fb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b18fb-123">CommonParameters</span></span>
<span data-ttu-id="b18fb-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b18fb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b18fb-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b18fb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b18fb-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b18fb-126">INPUTS</span></span>

### <span data-ttu-id="b18fb-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b18fb-127">None</span></span>
<span data-ttu-id="b18fb-128">Não é possível canalizar a entrada para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b18fb-128">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="b18fb-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b18fb-129">OUTPUTS</span></span>

### <span data-ttu-id="b18fb-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b18fb-130">None</span></span>
<span data-ttu-id="b18fb-131">Esse cmdlet não retorna nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="b18fb-131">This cmdlet does not return any output.</span></span>

## <span data-ttu-id="b18fb-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b18fb-132">NOTES</span></span>

## <span data-ttu-id="b18fb-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b18fb-133">RELATED LINKS</span></span>

[<span data-ttu-id="b18fb-134">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="b18fb-134">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="b18fb-135">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="b18fb-135">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="b18fb-136">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="b18fb-136">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="b18fb-137">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="b18fb-137">Remove-AzureAccount</span></span>](./Remove-AzureAccount.md)


