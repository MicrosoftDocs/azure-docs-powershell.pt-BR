---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/?view=azurermps-6.8.1
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppContainerPSSession.md
ms.openlocfilehash: 3c5efcd51a8b546acb5fa9b8ed3623c40ddfb1e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427085"
---
# <span data-ttu-id="89d26-101">New-AzureRmWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="89d26-101">New-AzureRmWebAppContainerPSSession</span></span>

## <span data-ttu-id="89d26-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89d26-102">SYNOPSIS</span></span>
<span data-ttu-id="89d26-103">New-AzureRmWebAppContainerPSSession criará uma nova sessão remota do PowerShell no contêiner do Windows especificado em determinado site ou slot e em um determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="89d26-103">New-AzureRmWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89d26-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89d26-104">SYNTAX</span></span>

### <span data-ttu-id="89d26-105">S1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="89d26-105">S1 (Default)</span></span>
```
New-AzureRmWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89d26-106">S2</span><span class="sxs-lookup"><span data-stu-id="89d26-106">S2</span></span>
```
New-AzureRmWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89d26-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="89d26-107">DESCRIPTION</span></span>
<span data-ttu-id="89d26-108">New-AzureRmWebAppContainerPSSession criará uma nova sessão remota do PowerShell no contêiner do Windows especificado em determinado site ou slot e em um determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="89d26-108">New-AzureRmWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="89d26-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89d26-109">EXAMPLES</span></span>

### <span data-ttu-id="89d26-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="89d26-110">Example 1</span></span>
```
PS C:\> $s = New-AzureRmWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="89d26-111">Isso criará uma nova sessão remota do PowerShell na ContosoASP do aplicativo de contêiner do Windows e mostrará os processos em execução no contêiner ContosoASP</span><span class="sxs-lookup"><span data-stu-id="89d26-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="89d26-112">OS</span><span class="sxs-lookup"><span data-stu-id="89d26-112">PARAMETERS</span></span>

### <span data-ttu-id="89d26-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89d26-113">-DefaultProfile</span></span>
<span data-ttu-id="89d26-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="89d26-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89d26-115">-Force</span><span class="sxs-lookup"><span data-stu-id="89d26-115">-Force</span></span>
<span data-ttu-id="89d26-116">Crie a sessão do PowerShell sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="89d26-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="89d26-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="89d26-117">-Name</span></span>
<span data-ttu-id="89d26-118">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="89d26-118">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89d26-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89d26-119">-ResourceGroupName</span></span>
<span data-ttu-id="89d26-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="89d26-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d26-121">-Slotname</span><span class="sxs-lookup"><span data-stu-id="89d26-121">-SlotName</span></span>
<span data-ttu-id="89d26-122">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="89d26-122">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89d26-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="89d26-123">-WebApp</span></span>
<span data-ttu-id="89d26-124">O objeto Web App</span><span class="sxs-lookup"><span data-stu-id="89d26-124">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89d26-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="89d26-125">-Confirm</span></span>
<span data-ttu-id="89d26-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89d26-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89d26-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89d26-127">-WhatIf</span></span>
<span data-ttu-id="89d26-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="89d26-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89d26-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="89d26-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89d26-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89d26-130">CommonParameters</span></span>
<span data-ttu-id="89d26-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89d26-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89d26-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89d26-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89d26-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="89d26-133">INPUTS</span></span>

### <span data-ttu-id="89d26-134">System. String</span><span class="sxs-lookup"><span data-stu-id="89d26-134">System.String</span></span>
### <span data-ttu-id="89d26-135">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="89d26-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>
## <span data-ttu-id="89d26-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="89d26-136">OUTPUTS</span></span>

### <span data-ttu-id="89d26-137">System. String</span><span class="sxs-lookup"><span data-stu-id="89d26-137">System.String</span></span>
## <span data-ttu-id="89d26-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="89d26-138">NOTES</span></span>

## <span data-ttu-id="89d26-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89d26-139">RELATED LINKS</span></span>
