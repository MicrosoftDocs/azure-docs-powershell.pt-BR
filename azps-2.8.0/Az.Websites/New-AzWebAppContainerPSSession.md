---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
ms.openlocfilehash: 651ca91a8da5a025040127b4e3bbcedf16225faf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772375"
---
# <span data-ttu-id="ac635-101">New-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="ac635-101">New-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="ac635-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ac635-102">SYNOPSIS</span></span>
<span data-ttu-id="ac635-103">New-AzWebAppContainerPSSession criará uma nova sessão remota do PowerShell no contêiner do Windows especificado em determinado site ou slot e em um determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ac635-103">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="ac635-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac635-104">SYNTAX</span></span>

### <span data-ttu-id="ac635-105">S1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="ac635-105">S1 (Default)</span></span>
```
New-AzWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac635-106">S2</span><span class="sxs-lookup"><span data-stu-id="ac635-106">S2</span></span>
```
New-AzWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac635-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ac635-107">DESCRIPTION</span></span>
<span data-ttu-id="ac635-108">New-AzWebAppContainerPSSession criará uma nova sessão remota do PowerShell no contêiner do Windows especificado em determinado site ou slot e em um determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ac635-108">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="ac635-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ac635-109">EXAMPLES</span></span>

### <span data-ttu-id="ac635-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ac635-110">Example 1</span></span>
```
PS C:\> $s = New-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="ac635-111">Isso criará uma nova sessão remota do PowerShell na ContosoASP do aplicativo de contêiner do Windows e mostrará os processos em execução no contêiner ContosoASP</span><span class="sxs-lookup"><span data-stu-id="ac635-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="ac635-112">OS</span><span class="sxs-lookup"><span data-stu-id="ac635-112">PARAMETERS</span></span>

### <span data-ttu-id="ac635-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac635-113">-DefaultProfile</span></span>
<span data-ttu-id="ac635-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ac635-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac635-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ac635-115">-Force</span></span>
<span data-ttu-id="ac635-116">Crie a sessão do PowerShell sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="ac635-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ac635-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac635-117">-Name</span></span>
<span data-ttu-id="ac635-118">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="ac635-118">The name of the web app.</span></span>

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

### <span data-ttu-id="ac635-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac635-119">-ResourceGroupName</span></span>
<span data-ttu-id="ac635-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ac635-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="ac635-121">-Slotname</span><span class="sxs-lookup"><span data-stu-id="ac635-121">-SlotName</span></span>
<span data-ttu-id="ac635-122">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="ac635-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="ac635-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ac635-123">-WebApp</span></span>
<span data-ttu-id="ac635-124">O objeto Web App</span><span class="sxs-lookup"><span data-stu-id="ac635-124">The web app object</span></span>

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

### <span data-ttu-id="ac635-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ac635-125">-Confirm</span></span>
<span data-ttu-id="ac635-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac635-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac635-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac635-127">-WhatIf</span></span>
<span data-ttu-id="ac635-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ac635-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac635-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ac635-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac635-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac635-130">CommonParameters</span></span>
<span data-ttu-id="ac635-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac635-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac635-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac635-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac635-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ac635-133">INPUTS</span></span>

### <span data-ttu-id="ac635-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ac635-134">System.String</span></span>

### <span data-ttu-id="ac635-135">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="ac635-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ac635-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ac635-136">OUTPUTS</span></span>

### <span data-ttu-id="ac635-137">System. Management. Automation. Runspaces. PSSession</span><span class="sxs-lookup"><span data-stu-id="ac635-137">System.Management.Automation.Runspaces.PSSession</span></span>

## <span data-ttu-id="ac635-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ac635-138">NOTES</span></span>

## <span data-ttu-id="ac635-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac635-139">RELATED LINKS</span></span>