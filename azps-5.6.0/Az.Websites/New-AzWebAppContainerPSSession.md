---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
ms.openlocfilehash: 213fbd5e035c48892db1c44fb4ac8de8fbf8bba9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887276"
---
# <span data-ttu-id="b9ce0-101">New-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="b9ce0-101">New-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="b9ce0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9ce0-102">SYNOPSIS</span></span>
<span data-ttu-id="b9ce0-103">New-AzWebAppContainerPSSession criará nova Sessão remota do PowerShell no contêiner do Windows especificado em um determinado site ou slot e determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b9ce0-103">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="b9ce0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b9ce0-104">SYNTAX</span></span>

### <span data-ttu-id="b9ce0-105">S1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b9ce0-105">S1 (Default)</span></span>
```
New-AzWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9ce0-106">S2</span><span class="sxs-lookup"><span data-stu-id="b9ce0-106">S2</span></span>
```
New-AzWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9ce0-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b9ce0-107">DESCRIPTION</span></span>
<span data-ttu-id="b9ce0-108">New-AzWebAppContainerPSSession criará nova Sessão remota do PowerShell no contêiner do Windows especificado em um determinado site ou slot e determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b9ce0-108">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="b9ce0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9ce0-109">EXAMPLES</span></span>

### <span data-ttu-id="b9ce0-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b9ce0-110">Example 1</span></span>
```
PS C:\> $s = New-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="b9ce0-111">Isso criará uma nova Sessão remota do PowerShell no aplicativo de contêiner do Windows ContosoASP e mostrará os processos que estão sendo executados no contêiner ContosoASP</span><span class="sxs-lookup"><span data-stu-id="b9ce0-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="b9ce0-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b9ce0-112">PARAMETERS</span></span>

### <span data-ttu-id="b9ce0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9ce0-113">-DefaultProfile</span></span>
<span data-ttu-id="b9ce0-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ce0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9ce0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b9ce0-115">-Force</span></span>
<span data-ttu-id="b9ce0-116">Crie a sessão do PowerShell sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="b9ce0-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b9ce0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b9ce0-117">-Name</span></span>
<span data-ttu-id="b9ce0-118">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="b9ce0-118">The name of the web app.</span></span>

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

### <span data-ttu-id="b9ce0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9ce0-119">-ResourceGroupName</span></span>
<span data-ttu-id="b9ce0-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b9ce0-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="b9ce0-121">-SlotName</span><span class="sxs-lookup"><span data-stu-id="b9ce0-121">-SlotName</span></span>
<span data-ttu-id="b9ce0-122">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="b9ce0-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="b9ce0-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b9ce0-123">-WebApp</span></span>
<span data-ttu-id="b9ce0-124">O objeto do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="b9ce0-124">The web app object</span></span>

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

### <span data-ttu-id="b9ce0-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9ce0-125">-Confirm</span></span>
<span data-ttu-id="b9ce0-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9ce0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9ce0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9ce0-127">-WhatIf</span></span>
<span data-ttu-id="b9ce0-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b9ce0-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9ce0-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b9ce0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9ce0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9ce0-130">CommonParameters</span></span>
<span data-ttu-id="b9ce0-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9ce0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9ce0-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9ce0-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9ce0-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9ce0-133">INPUTS</span></span>

### <span data-ttu-id="b9ce0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b9ce0-134">System.String</span></span>

### <span data-ttu-id="b9ce0-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="b9ce0-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b9ce0-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b9ce0-136">OUTPUTS</span></span>

### <span data-ttu-id="b9ce0-137">System.Management.Automation.Runspaces.PSSession</span><span class="sxs-lookup"><span data-stu-id="b9ce0-137">System.Management.Automation.Runspaces.PSSession</span></span>

## <span data-ttu-id="b9ce0-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="b9ce0-138">NOTES</span></span>

## <span data-ttu-id="b9ce0-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9ce0-139">RELATED LINKS</span></span>
